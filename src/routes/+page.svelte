<script>
	import Button from '$lib/Button.svelte';
	import Window from '$lib/Window.svelte';

	let count = $state(0);

	function increment() {
		count += 1;
	}
</script>

<Window>
	{#snippet label()}
		Click Counter
	{/snippet}
	{#snippet icon()}
		<svg width="24" height="24" viewBox="0 0 24 24">
			<circle stroke="#ccc" fill="none" cx="12" cy="12" r="8" />
		</svg>
	{/snippet}
	<Button onclick={increment}>
		{#snippet icon()}
			<svg width="24" height="24" viewBox="0 0 24 24">
				<circle stroke="#ccc" fill="none" cx="12" cy="12" r="8" />
			</svg>
		{/snippet}
		{#snippet label()}
			Clicks: {count}
		{/snippet}
	</Button>
</Window>
