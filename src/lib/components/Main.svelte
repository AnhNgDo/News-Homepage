<script>
	import hero from '$lib/images/image-web-3-desktop.jpg';

	export let newsTitles;
</script>

<div class="flex flex-col gap-6 sm:flex-row">
	<!-- Hero -->
	<div class="flex flex-col gap-2">
		<img src={hero} alt="hero" class="h-96 w-96 sm:h-auto sm:w-auto" />
		<div class="flex flex-col justify-between gap-2 sm:flex-row">
			<h1 class="basis-1/3 text-5xl font-black sm:text-7xl ">The bright future of Web 3.0?</h1>
			<div class="flex basis-1/3 flex-col flex-wrap justify-between gap-3">
				<p class="sm:text-xl">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus, placeat commodi?
					Dolorum nam earum in enim natus expedita fugit ut praesentium. Temporibus fugit sequi
					suscipit.
				</p>
				<button class="btn w-1/3 rounded-none bg-red-400">Read More</button>
			</div>
		</div>
	</div>

	<!-- News -->
	<div class="flex flex-col gap-8 bg-gray-700 p-8 text-white">
		<h1 class="text-4xl font-bold text-yellow-500">NEWS</h1>
		<div class=" flex basis-3/4 flex-col justify-around">
			{#each newsTitles as title}
				<section>
					<h2 class="text-2xl font-semibold">{title}</h2>
					<p class="opacity-50">
						Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur, deleniti minima
						velit dolorum excepturi odio.
					</p>
					<hr class="m-8 align-middle opacity-50" />
				</section>
			{/each}
		</div>
	</div>
</div>
