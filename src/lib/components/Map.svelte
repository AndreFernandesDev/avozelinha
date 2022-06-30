<script lang="ts">
	import Text from '$lib/components/Text.svelte';
	import Container from '$lib/components/Container.svelte';
	import Wheat from '$lib/icons/Wheat.svelte';
	import Spacing from './Spacing.svelte';
	import Border from '$lib/icons/Border.svelte';
	import { Map, Marker } from '@beyonk/svelte-mapbox';
	let mapComponent: any;
	let zoom: number;

	function onReady() {
		zoom = 16;
		mapComponent.setCenter([-7.925, 37.025], 3);
		mapComponent.flyTo({ center: [-7.925, 37.026] });
	}
</script>

<section>
	<Container>
		<div id="content">
			<Text type="h2" fontSize={'3.5rem'} fontType={'Kraft'}>VISITE A NOSSA PASTELARIA</Text>
			<Spacing spacing="--mg-lg" />
		</div>
	</Container>
	<div id="borderTop">
		<Border />
	</div>
	<div id="map">
		<div id="mapboxContent">
			<Map
				accessToken="pk.eyJ1IjoiYW5kcmVwaW5oZWlybyIsImEiOiJja3pmd3cybDQyd2Z0Mm5uOXJwb3NhaHVwIn0.0YMimqM8uPJFgEV6Al6rug"
				style="mapbox://styles/mapbox/outdoors-v11"
				bind:this={mapComponent}
				bind:zoom
				on:ready={onReady}
			>
				<Marker lat="37.0258" lng="-7.9255" label="Avo Zelinha" />
			</Map>
		</div>
	</div>
	<div id="borderBottom">
		<Border />
	</div>
	<div id="wheatLeft">
		<Wheat />
	</div>
	<div id="wheatRight">
		<Wheat />
	</div>
</section>

<style>
	section {
		position: relative;
		margin-bottom: var(--mg-lg);
	}

	#content {
		text-align: center;
	}

	#map {
		display: block;
		height: 300px;
		width: 100%;
	}

	#mapboxContent {
		width: 100%;
		height: 300px;
		position: absolute;
		z-index: -99;
	}

	#borderBottom {
		transform: scaleY(-1);
	}

	#wheatLeft {
		position: absolute;
		top: 100px;
		left: 0;
	}

	#wheatRight {
		position: absolute;
		top: 100px;
		right: 0;
		transform: scaleX(-1);
	}
</style>
