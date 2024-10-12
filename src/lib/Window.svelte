<script>
	const { label, icon, children } = $props();
</script>

<div class="window">
	<div class="head">
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
	</div>
	<div class="body">
		{#if children}
			{@render children()}
		{/if}
	</div>
</div>

<style>
	.window {
		border: solid 1px #ccc;
	}
	.head {
		display: flex;
		align-items: center;
		padding: 10px;
		gap: 5px;
	}
	.icon,
	.label {
		display: flex;
		align-items: center;
	}
	.body {
		padding: 10px;
	}
</style>
