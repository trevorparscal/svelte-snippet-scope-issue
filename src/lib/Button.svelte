<script>
	const { icon, label, onclick = $bindable() } = $props();
</script>

<button class="button" {onclick}>
	{#if icon}
		<span class="icon">
			{@render icon()}
		</span>
	{/if}
	{#if label}
		<span class="label">
			{@render label()}
		</span>
	{/if}
</button>

<style>
	.button {
		display: flex;
		align-items: center;
		gap: 5px;
	}
	.icon,
	.label {
		display: flex;
		align-items: center;
	}
</style>
