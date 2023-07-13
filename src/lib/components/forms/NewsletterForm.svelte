<script lang="ts">
	import { fade } from 'svelte/transition';

	export let placeholder: string = 'Enter your email';
	export let email: string = '';
	export let buttonLabel = 'Subscribe';

	const expression: RegExp = /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i;
	let errorMessage = '';
	let showError = false;

	function validateEmail() {
		if (!email) {
			errorMessage = 'Email is required';
			showError = true;
		} else if (!expression.test(email)) {
			errorMessage = 'Invalid email format';
			showError = true;
		} else {
			errorMessage = '';
			showError = false;
			// Additional logic for submitting the form
		}
	}

	function handleSubmit(event: Event) {
		event.preventDefault();
		validateEmail();
	}

	function handleInput() {
		errorMessage = '';
		showError = false;
	}
</script>

<form
	on:submit={handleSubmit}
	class="flex flex-col gap-2 items-center justify-center text-center w-full"
>
	<div class="flex flex-row relative">
		{#if showError}
			<div transition:fade class=" absolute -top-6 left-0 text-red">{errorMessage}</div>
		{/if}
		<input
			type="email"
			bind:value={email}
			on:input={handleInput}
			{placeholder}
			class="border {showError
				? 'border-red '
				: 'border-gray-300'} px-4 py-3 bg-gray-50 rounded-l-lg md:min-w-[21.5rem]"
		/>

		<div class="bg-blue-600 border border-blue-600 py-3 px-5 rounded-r-lg text-white">
			<button type="submit">{buttonLabel}</button>
		</div>
	</div>
	<p class="text-sm text-gray-500">
		We care about the protection of your data. Read our <a href="/" class="underline text-gray-900"
			>Privacy Policy.</a
		>
	</p>
</form>
