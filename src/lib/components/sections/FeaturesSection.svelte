<script lang="ts">
	import FeatureCard from '../cards/FeatureCard.svelte';

	export let headline: string = 'Designed for business teams like yours';
	export let subHeadline: string =
		'Here at flowbite we focus on markets where technology, innovation, and capital can unlock long-term value and drive economic growth.';
	export let features: Array<{ title: string; description: string; iconUrl: string }> = [
		{
			title: 'Marketing',
			description:
				'Plan it, create it, launch it. Collaborate seamlessly with all  the organization and hit your marketing goals every month with our marketing plan.',
			iconUrl: 'src/lib/assets/icons/presentation-chart-line.svg'
		},
		{
			title: 'Legal',
			description:
				'Protect your organization, devices and stay compliant with our structured workflows and custom permissions made for you.',
			iconUrl: 'src/lib/assets/icons/academic-cap.svg'
		},
		{
			title: 'Business Automation',
			description:
				'Auto-assign tasks, send Slack messages, and much more. Now power up with hundreds of new templates to help you get started.',
			iconUrl: 'src/lib/assets/icons/briefcase.svg'
		}
	];
</script>

<section class="flex flex-col gap-12 w-full px-8 py-12 md:px-20 md:py-24">
	<div class="flex flex-col gap-4">
		<h2 class="text-4xl text-gray-900">{headline}</h2>
		<h5 class="text-lg text-gray-500">
			{subHeadline}
		</h5>
	</div>
	<div class="flex md:flex-row flex-col w-full items-stretch justify-evenly gap-12">
		{#each features as feature}
			<FeatureCard
				iconUrl={feature.iconUrl}
				title={feature.title}
				description={feature.description}
			/>
		{/each}
	</div>
</section>
