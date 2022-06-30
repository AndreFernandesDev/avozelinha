<script lang="ts">
	export let type: string;

	import Cupcake from '$lib/icons/Cupcake.svelte';
	import SliceCake from '$lib/icons/SliceCake.svelte';
	import Bread from '$lib/icons/Bread.svelte';
</script>

{#if type === 'Cupcake'}
	<Cupcake />
{:else if type === 'SliceCake'}
	<SliceCake />
{:else if type === 'Bread'}
	<Bread />
{/if}
