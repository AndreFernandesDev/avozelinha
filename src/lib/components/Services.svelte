<script lang="ts">
	import SingleService from '$lib/components/SingleService.svelte';
	import Container from '$lib/components/Container.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
	import Text from '$lib/components/Text.svelte';

	type ImageSettings = {
		width?: string;
	};
	type Service = {
		title: string;
		types: Array<string>;
		img: string;
		imgSettings?: ImageSettings;
	};

	const services: Array<Service> = [
		{
			title: 'Semi Frios',
			types: ['Semi Frios', 'Bolos Secos', 'Bolas de berlim'],
			img: 'Cupcake'
		},
		{
			title: 'Semi Frios',
			types: ['Semi Frios', 'Bolos Secos', 'Bolas de berlim'],
			img: 'SliceCake',
			imgSettings: {
				width: '75%'
			}
		},
		{
			title: 'Semi Frios',
			types: ['Semi Frios', 'Bolos Secos', 'Bolas de berlim'],
			img: 'Bread',
			imgSettings: {
				width: '80%'
			}
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
				<SingleService
					title={service.title}
					types={service.types}
					img={service.img}
					imgSettings={service.imgSettings}
				/>
			{/each}
		</div>
	</Container>
</section>

<style>
	#content {
		justify-content: center;
	}
</style>
