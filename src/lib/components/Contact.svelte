<script lang="ts">
	import Container from '$lib/components/Container.svelte';
	import Text from '$lib/components/Text.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
	import String from '$lib/icons/String.svelte';
	import Form from '$lib/components/Form.svelte';
</script>

<section>
	<Container>
		<div id="content">
			<Text type="h2" fontType={'Kraft'} fontSize={'2rem'}>Fale Connosco</Text>
			<Text type="h3" fontType={'Chalk'} fontSize={'1.2rem'}>Queremos ajudar</Text>
			<Spacing spacing={'--mg-sm'} />
			<Form />
		</div>
	</Container>
	<div id="image">
		<String />
	</div>
</section>

<style>
	section {
		position: relative;
	}

	#content {
		width: 70%;
		flex-wrap: wrap;
		flex-direction: column;
	}

	#image {
		position: absolute;
		right: 0;
		top: 0px;
		z-index: -99;
	}
</style>
