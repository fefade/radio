<script lang="ts">
	let { children } = $props()
</script>

<div class="layout">
	<main class="content">
		{@render children()}
	</main>
</div>

<style>
	.layout {
		display: grid;
		grid-template-rows: auto 1fr auto;
		grid-template-areas:
			"content"
			"spacer"
			"footer";
		width: 1000px;
		margin: 0 auto;
		min-height: 100vh;
		gap: 1rem;
		padding: 3rem 0;
	}

	.content {
		grid-area: content;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	@media screen and (max-width: 768px) {
		.layout {
			width: 90%;
		}
	}
</style>
