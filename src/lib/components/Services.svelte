<script lang="ts">
	import SingleService from '$lib/components/SingleService.svelte';
	import Container from '$lib/components/Container.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
	import Text from '$lib/components/Text.svelte';

	type Service = {
		title: string;
		description: string;
	};

	const services: Array<Service> = [
		{
			title: 'Semi Frios',
			description: 'Empresa especializada na prevenção e controlo de pragas.'
		},
		{
			title: 'Convetaria',
			description: 'Empresa especializada na prevenção e controlo de pragas.'
		},
		{
			title: 'Desbaratizacao',
			description: 'Empresa especializada na prevenção e controlo de pragas.'
		},
		{
			title: 'Desbaratizacao',
			description: 'Empresa especializada na prevenção e controlo de pragas.'
		},
		{
			title: 'Desbaratizacao',
			description: 'Empresa especializada na prevenção e controlo de pragas.'
		}
	];
</script>

<section>
	<Spacing spacing="--mg-lg" />

	<Container>
		<div id="content">
			<Text type="h2" fontType="Kraft">Especialidades</Text>
			<Spacing spacing="--mg-lg" />
			{#each services as service}
				<SingleService title={service.title} description={service.description} />
			{/each}
		</div>
	</Container>
</section>

<style>
	#content {
		justify-content: center;
	}
</style>
