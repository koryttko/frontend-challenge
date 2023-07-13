<script lang="ts">
	import CtaButton from '../buttons/CtaButton.svelte';

	export let headline: string = "We invest in world's potential";
	export let subHeadline: string =
		'Here at flowbite we focus on markets where technology, innovation, and capital can unlocklong-term value and drive economic growth.';
</script>

<section
	class="flex md:flex-row flex-col items-center justify-center overflow-hidden w-full px-8 md:px-0 pt-24 md:pt-0"
>
	<div class="items-center justify-center text-center md:pl-20">
		<div class="flex flex-col gap-6">
			<h1 class="text-6xl text-gray-900">{headline}</h1>
			<h4 class="text-xl text-gray-500">{subHeadline}</h4>
		</div>
		<div class="flex flex-row gap-4 items-center justify-center pt-8 text-center">
			<CtaButton text="Learn more" iconUrl="src/lib/assets/icons/arrow-right.svg" hasIcon={true} />
			<CtaButton
				text="Watch video"
				iconLeft={true}
				iconUrl="src/lib/assets/icons/video-camera.svg"
				hasIcon={true}
				outlined={true}
				textColor="gray-800"
			/>
		</div>
	</div>
	<div class="-mr-40 max-w-sm md:max-w-fit">
		<img class="" src="src/lib/assets/images/header_image.png" alt="Hero" />
	</div>
</section>
