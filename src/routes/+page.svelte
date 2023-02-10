<script>
	import Navbar from '$lib/components/Navbar.svelte';
	import Main from '$lib/components/Main.svelte';
	import Card from '../lib/components/Card.svelte';
	import pc from '$lib/images/image-retro-pcs.jpg';
	import laptop from '$lib/images/image-top-laptops.jpg';
	import gaming from '$lib/images/image-gaming-growth.jpg';

	let menuItems = ['Home', 'New', 'Popular', 'Trending', 'Categories'];
	let newsTitles = [
		'Hydrogen vs Electric Cars',
		'The Downside of AI Art',
		'Is VC funding drying up?'
	];
	let data = [
		{
			imgSrc: pc,
			index: '01',
			title: 'Reviving Retro PCs',
			text: 'What happens when old PCs given upgrades?'
		},
		{
			imgSrc: laptop,
			index: '02',
			title: 'Top 10 laptops of 2022',
			text: 'Our best picks for various needs and budgets'
		},
		{
			imgSrc: gaming,
			index: '03',
			title: 'The Growth of Gaming',
			text: 'How the pandemic has sparked new opportunities'
		}
	];
</script>

<Navbar {menuItems} />
<Main {newsTitles} />

<!-- featured cards -->
<div class="my-8 grid grid-cols-1 gap-4 sm:my-20 sm:grid-cols-3">
	{#each data as article}
		<Card {...article} />
	{/each}
</div>

<!-- <style>
	div * {
		border: 1px;
		border-color: rgb(0 0 0);
		border-style: solid;
	}
</style> -->
