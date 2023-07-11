<script lang="ts">
	let companyLogosUrl: Array<string> = [
		'src/lib/assets/images/Google.svg',
		'src/lib/assets/images/Mailchimp.svg',
		'src/lib/assets/images/Microsoft.svg',
		'src/lib/assets/images/Spotify.svg'
	];
</script>

<section class="px-24 py-20">
	<div class="flex flex-col w-full items-center justify-center text-center gap-12">
		<h3>You'll be in good company</h3>
		<div class="flex flex-row flex-wrap items-center justify-center gap-14">
			{#each companyLogosUrl as companyLogoUrl}
				<img src={companyLogoUrl} alt="Company Logo" />
			{/each}
		</div>
	</div>
</section>
