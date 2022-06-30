<script lang="ts">
	type ImageSettings = {
		width?: string;
	};

	export let title: string;
	export let types: Array<string>;
	export let img: string;
	export let imgSettings: ImageSettings = {};

	import Text from '$lib/components/Text.svelte';
	import ServicesType from '$lib/icons/ServicesType.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
</script>

<div id="wrapper">
	<div id="icon">
		<img id="ring" src="/images/ring.png" alt="" />
		<div id="image" style="width:{imgSettings.width ? imgSettings.width : ''}">
			<ServicesType type={img} />
		</div>
	</div>
	<div id="content">
		<Text type="h3" fontSize={'2rem'} fontType={'Chalk'}>{title}</Text>
		<Spacing spacing="--mg-md" />
		<ul>
			{#each types as type}
				<li>&#8226; {type}</li>
			{/each}
		</ul>
	</div>
</div>

<style>
	li {
		font-size: 1.1rem;
		margin-bottom: var(--mg-sm);
	}

	#ring {
		height: 100%;
		border-radius: 8px;
		position: absolute;
		top: 0;
		left: -40%;
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
		justify-content: center;
		width: 55%;
		min-height: 250px;
	}

	#icon {
		width: 45%;
		position: relative;
		align-items: center;
	}

	#image {
		position: absolute;
		width: 60%;
		left: -20%;
	}
</style>
