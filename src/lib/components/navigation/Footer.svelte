<script lang="ts">
	export let copyright: string = '© 2021 Flowbite, LLC. All rights reserved.';
	export let socialLinks: Array<string> = [
		'src/lib/assets/icons/facebook-f.svg',
		'src/lib/assets/icons/twitter.svg',
		'src/lib/assets/icons/github.svg',
		'src/lib/assets/icons/dribbble.svg'
	];
</script>

<footer class="flex flex-row flex-wrap justify-between py-12 px-8 md:px-20 gap-4">
	<p class="text-gray-500">{copyright}</p>
	<div class="flex flex-row gap-6">
		{#each socialLinks as socialLink}
			<a href="/"><img src={socialLink} alt="Social Link" /></a>
		{/each}
	</div>
</footer>
