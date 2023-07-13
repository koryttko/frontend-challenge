<script lang="ts">
	export let images: Array<string>;
</script>

<div class="grid gap-4 items-stretch w-full">
	{#each images as image}
		<img class="h-[240px] w-full rounded-lg object-cover" src={image} alt="description" />
	{/each}
</div>

<style>
	.grid {
		grid-template-columns: repeat(4, 1fr);
		grid-template-areas:
			'image1 image1 image2 image3'
			'image4 image5 image5 image6';
	}

	img:nth-child(1) {
		grid-area: image1;
	}
	img:nth-child(2) {
		grid-area: image2;
	}
	img:nth-child(3) {
		grid-area: image3;
	}
	img:nth-child(4) {
		grid-area: image4;
	}
	img:nth-child(5) {
		grid-area: image5;
	}
	img:nth-child(6) {
		grid-area: image6;
	}
</style>
