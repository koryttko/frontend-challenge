<script lang="ts">
	export let iconUrl: string;
	export let title: string;
	export let description: string;
</script>

<div class="flex flex-col gap-4">
	<div class="rounded-full w-12 h-12 flex flex-row justify-center items-center bg-[#E2E4EB]">
		<img src={iconUrl} alt="Icon" class="w-8 h-8" />
	</div>
	<div class="flex flex-col gap-2">
		<h4 class="text-xl text-gray-900">{title}</h4>
		<p class="text-gray-500">{description}</p>
	</div>
</div>
