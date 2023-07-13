<script lang="ts">
	import NewsletterForm from '../forms/NewsletterForm.svelte';

	export let headline: string = 'Sign up for our newsletter';
	export let description: string =
		'Stay up to date with the roadmap progress, announcements and exclusive discounts feel free to sign up with your email.';
</script>

<section
	class="flex flex-col items-center justify-center text-center py-12 md:py-24 px-8 md:px-20 gap-8"
>
	<div class="flex flex-col max-w-2xl gap-4">
		<h2 class="text-4xl text-gray-900">{headline}</h2>
		<h5 class="text-lg text-gray-500">
			{description}
		</h5>
	</div>
	<NewsletterForm />
</section>
