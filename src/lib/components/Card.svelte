<script>
	import pc from '$lib/images/image-retro-pcs.jpg';

	export let imgSrc;
	export let index;
	export let title;
	export let text;
</script>

<div class="flex flex-row gap-4 sm:gap-10">
	<img src={imgSrc} alt="retro pcs" class="w-1/3 sm:w-auto" />
	<div class="flex basis-full flex-col justify-between">
		<p class="text-4xl font-bold text-gray-300 sm:text-8xl">{index}</p>
		<h3 class="text-2xl font-bold sm:text-3xl">{title}</h3>
		<p class="text-lg opacity-70 sm:text-xl">{text}</p>
	</div>
</div>
