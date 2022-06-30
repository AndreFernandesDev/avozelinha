<script lang="ts">
	export let type: string = 'p';
	export let fontSize: string = '';
	export let fontType: string = '';
</script>

{#if type === 'h1'}
	<h1 style:--fontSize={fontSize ? fontSize : '1rem'} style:--font={fontType}><slot /></h1>
{:else if type === 'h2'}
	<h2 style:--fontSize={fontSize ? fontSize : '3.5rem'} style:--font={fontType}><slot /></h2>
{:else if type === 'h3'}
	<h3 style:--fontSize={fontSize ? fontSize : '.8rem'} style:--font={fontType}><slot /></h3>
{:else if type === 'h4'}
	<h4 style:--fontSize={fontSize ? fontSize : '.625rem'} style:--font={fontType}><slot /></h4>
{:else if type === 'h5'}
	<h5 style:--fontSize={fontSize ? fontSize : '.625rem'} style:--font={fontType}><slot /></h5>
{:else}
	<p style:--fontSize={fontSize ? fontSize : '.8rem'} style:--font={fontType}><slot /></p>
{/if}

<style>
	h1 {
		--fontType: var(--font);
		font-family: var(--fontType);
		font-style: normal;
		font-weight: 500;
		font-size: var(--fontSize);
		line-height: var(--fontSize);
		text-transform: uppercase;
	}

	h2 {
		--fontType: var(--font);
		font-family: var(--fontType);
		font-style: normal;
		font-weight: 500;
		font-size: var(--fontSize);
		line-height: var(--fontSize);
		text-transform: uppercase;
	}

	h3 {
		--fontType: var(--font);
		font-family: var(--fontType);
		font-style: normal;
		font-weight: 500;
		font-size: var(--fontSize);
		line-height: var(--fontSize);
	}

	h4 {
		--fontType: var(--font);
		font-family: var(--fontType);
		font-style: normal;
		font-weight: 500;
		font-size: var(--fontSize);
		line-height: var(--fontSize);
	}

	h5 {
		--fontType: var(--font);
		font-family: var(--fontType);
		font-style: normal;
		font-weight: 500;
		font-size: var(--fontSize);
		line-height: var(--fontSize);
	}

	p {
		--fontType: var(--font);
		font-family: var(--fontType);
		font-style: normal;
		font-weight: 300;
		font-size: var(--fontSize);
		line-height: 150%;
	}
</style>
