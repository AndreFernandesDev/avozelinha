<script lang="ts">
	export let fontSize: string = '1rem';
	export let type: string = '';
</script>

{#if type === 'call'}
	<a href="tel:965-710-575"><button style:--fontSize={fontSize}><slot /></button></a>
{:else}
	<button style:--fontSize={fontSize}><slot /></button>
{/if}

<style>
	button {
		background: var(--primary);
		color: var(--dark);
		font-family: var(--fontType);
		font-size: var(--fontSize);
		padding: 0.3em 1.25em;
		display: flex;
		background: linear-gradient(93.18deg, #f4e2ce 0%, #eae1d6 100%);
		box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.7);
		border-radius: 6px;
		letter-spacing: -0.1em;
	}

	a {
		text-decoration: none;
	}
</style>
