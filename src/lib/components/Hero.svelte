<script lang="ts">
	import Container from '$lib/components/Container.svelte';
	import Text from '$lib/components/Text.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
	import String from '$lib/icons/String.svelte';
	import Button from '$lib/components/Button.svelte';
</script>

<section>
	<Container>
		<div id="content">
			<div id="text">
				<Text type="h2" fontType="Kraft" fontSize={'2.75rem'}>Descubra sabores farenses</Text>
				<Spacing spacing={'--mg-sm'} />
				<Text type="h3" fontType="Chalk" fontSize={'1.3rem'}>Algum texto vai aqui</Text>
				<Spacing spacing={'--mg-md'} />
				<div id="button">
					<Button type={'call'}>Encomende ja</Button>
				</div>
			</div>

			<img id="logo" src="images/logo.png" alt="PestZero" />
		</div>
		<div id="decoration">
			<String />
		</div>
	</Container>
</section>

<style>
	section {
		padding-top: var(--mg-lg);
		position: relative;
	}

	#content {
		align-items: flex-start;
	}

	#text {
		width: 55%;
		flex-wrap: wrap;
	}

	img {
		object-fit: contain;
		width: 45%;
	}

	#decoration {
		position: absolute;
		right: 0;
		bottom: 32px;
	}
</style>
