<script lang="ts">
	import Container from './Container.svelte';
	import Button from './Button.svelte';
	import Phone from '$lib/icons/Phone.svelte';
	import Burger from '$lib/icons/Burger.svelte';
	import Text from './Text.svelte';
</script>

<Container>
	<nav>
		<Text type="h1" fontType="Handy">FARO | PENHA</Text>
		<Burger />
	</nav>
</Container>

<style>
	nav {
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-top: var(--mg-md);
	}

	#logo {
		height: 50px;
		object-fit: contain;
	}

	#icon {
		width: 19px;
		height: 19px;
		object-fit: contain;
		margin-left: var(--mg-sm);
	}
</style>
