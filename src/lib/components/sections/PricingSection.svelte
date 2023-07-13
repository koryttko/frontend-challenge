<script lang="ts">
	import { onMount } from 'svelte';

	export let headline: string = 'Designed for business teams like yours';
	export let subHeadline: string =
		'Here at flowbite we focus on markets where technology, innovation, and capital can unlock long-term value and drive economic growth.';

	let result: any;

	onMount(async function () {
		const response = await fetch('https://n8n.thearc.dev/webhook/pricing', {
			method: 'POST',
			headers: {
				'content-type': 'application/json'
			},
			body: JSON.stringify({ interval: 'monthly' })
		});
		const json = await response.json();
		result = json;
		console.log('---------RESULT------------:', result);
	});
</script>

<section class="flex flex-col pt-16 pb-24 py-20">
	<div class="flex flex-col items-center justify-center text-center gap-4">
		<h2 class="text-4xl text-gray-900">{headline}</h2>
		<h5 class="text-lg text-gray-500">{subHeadline}</h5>
	</div>
</section>
