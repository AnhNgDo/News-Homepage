<script>
	import logo from '$lib/images/logo.svg';
	import menu from '$lib/images/icon-menu.svg';
	import menuClose from '$lib/images/icon-menu-close.svg';
	import { fly, scale } from 'svelte/transition';
	import { quadOut } from 'svelte/easing';

	export let menuItems;
	let open = false;

	function toggle() {
		open = !open;
	}
</script>

<nav class="flex flex-row justify-between">
	<img src={logo} alt="logo" class="my-8" />
	<div class="hidden sm:my-8 sm:flex sm:flex-row">
		{#each menuItems as item}
			<p class="mx-4 list-none hover:text-blue-600/30">
				{item}
			</p>
		{/each}
	</div>

	<img
		src={open ? menuClose : menu}
		alt="mobile-menu"
		class="my-8 h-10 w-10 sm:hidden"
		on:click={toggle}
		on:keydown={toggle}
	/>
</nav>

<!-- mobile drop down menu with animation -->
{#if open}
	<ul class="menu p-2 text-center">
		{#each menuItems as item, i}
			<li class="hover:underline" transition:fly={{ y: -15, delay: 50 * i }}>{item}</li>
		{/each}
	</ul>
	<!-- customise hr using Tailwind's border classes -->
	<hr class="mb-4 border-2" transition:scale={{ duration: 750, easing: quadOut }} />
{/if}
