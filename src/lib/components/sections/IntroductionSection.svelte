<script lang="ts">
	import ImageGrid from './../grids/ImageGrid.svelte';

	export let headline: string = "We didn't reinvent the wheel";
	export let subHeadline: string =
		'We are strategists, designers and developers. Innovators and problem solvers. Small enough to be simple and quick, but big enough to deliver the scope you want at the pace you need.';
	export let images: Array<string> = [
		'src/lib/assets/images/24e8710129501d39eebe8df995bc0eac.jpg',
		'src/lib/assets/images/d53e9fbd7876d2aea28fec579a914475.jpg',
		'src/lib/assets/images/03241163713451df4e0e12ebd3c437b7.jpg',
		'src/lib/assets/images/9bc6709b8da6763f544bc1d2a4b945a5.jpg',
		'src/lib/assets/images/28a3596b9f53d4315ba234b2dfd67583.jpg',
		'src/lib/assets/images/edb29eb0d5b3f9984d10e537914440db.jpg'
	];
</script>

<section
	class="flex flex-col items-center justify-center text-center pt-16 pb-12 md:pb-24 px-8 md:px-20 gap-12"
>
	<div class="flex flex-col gap-4 text-center items-center justify-center">
		<h2 class="text-4xl text-gray-900">{headline}</h2>
		<h5 class="text-lg text-gray-500 md:max-w-[80%]">{subHeadline}</h5>
	</div>
	<ImageGrid {images} />
</section>
