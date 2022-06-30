<script lang="ts">
	export let title: string;
	export let description: string;

	import Text from '$lib/components/Text.svelte';
	import Cupcake from '$lib/icons/Cupcake.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
</script>

<div id="wrapper">
	<div id="icon">
		<img id="ring" src="/images/ring.png" alt="" />
		<div id="image">
			<Cupcake />
		</div>
	</div>
	<div id="content">
		<Text type="h3" fontSize={'2rem'} fontType={'Chalk'}>{title}</Text>
		<Spacing spacing="--mg-sm" />
		<Text>{description}</Text>
	</div>
</div>

<style>
	#ring {
		height: 100%;
		border-radius: 8px;
		position: absolute;
		top: 0;
		left: -30%;
	}

	#wrapper {
		border-right: 5px solid var(--green);
		margin-bottom: var(--mg-md);
		width: 100%;
		align-items: stretch;
		position: relative;
		flex-wrap: nowrap;
	}

	#content {
		flex-direction: column;
		width: 50%;
		min-height: 250px;
	}

	#icon {
		width: 50%;
		position: relative;
		align-items: center;
	}

	#image {
		position: absolute;
		width: 60%;
		left: -20%;
	}
</style>
