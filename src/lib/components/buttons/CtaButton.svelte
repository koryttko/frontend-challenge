<script lang="ts">
	export let text: string;
	export let hasIcon: boolean;
	export let iconLeft: boolean = false;
	export let iconUrl: string = '';
	export let bgColor: string = 'blue-600';
	export let textColor: string = 'white';
	export let outlined: boolean = false;
</script>

<button
	class={`flex flex-row justify-center items-center w-fit px-6 py-[0.875rem] rounded-lg ${
		outlined ? 'bg-white border border-gray-300' : `bg-${bgColor}`
	}  text-${textColor}`}
>
	<div
		class="flex {iconLeft
			? 'flex-row-reverse'
			: 'flex-row'} text-nowrap gap-3 items-center justify-center"
	>
		{text}
		{#if hasIcon}
			<img src={iconUrl} alt="Icon" class="w-5 h-5" />
		{/if}
	</div>
</button>
