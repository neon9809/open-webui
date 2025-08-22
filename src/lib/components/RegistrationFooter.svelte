<script>
	import { onMount } from 'svelte';
	
	let registrationContent = '';
	let isLoading = true;
	let hasError = false;

	onMount(async () => {
		try {
			const response = await fetch('/external-static/registration.html');
			if (response.ok) {
				registrationContent = await response.text();
			} else {
				hasError = true;
			}
		} catch (error) {
			console.log('Registration info not found:', error);
			hasError = true;
		} finally {
			isLoading = false;
		}
	});
</script>

{#if !isLoading && !hasError && registrationContent}
	<div class="registration-info mt-4 text-xs text-gray-500 dark:text-gray-400 text-center">
		{@html registrationContent}
	</div>
{/if}

<style>
	.registration-info :global(a) {
		color: inherit;
		text-decoration: underline;
	}
	
	.registration-info :global(a:hover) {
		opacity: 0.8;
	}
</style>

