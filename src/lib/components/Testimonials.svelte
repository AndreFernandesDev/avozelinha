<script lang="ts">
	import Container from '$lib/components/Container.svelte';
	import Text from '$lib/components/Text.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
	import Slider from '$lib/components/Slider.svelte';

	type Company = {
		title: string;
		description: string;
	};

	const services: Array<Company> = [
		{
			title: 'Laura Lopes',
			description: 'Gostamos muito, fantastico.'
		},
		{
			title: 'Paulo Lopes',
			description: 'Delicioso, amigaveis, impressionantes.'
		},
		{
			title: 'Ana Lopes',
			description: 'Gostamos muito, fantastico.'
		},
		{
			title: 'Chefe Branco',
			description: 'Delicioso, amigaveis, impressionantes.'
		},
		{
			title: 'Marco Silva',
			description: 'Gostamos muito, fantastico.'
		}
	];
</script>

<section>
	<Container>
		<div id="content">
			<Text type="h2" fontType="Kraft">O QUE DIZEM</Text>
			<Slider items={services} />
		</div>
	</Container>
</section>
<Spacing spacing={'--mg-xl'} />

<style>
	section {
		position: relative;
		border-bottom: 3px solid var(--green);
	}

	#content {
		flex-wrap: wrap;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 100%;
	}
</style>
