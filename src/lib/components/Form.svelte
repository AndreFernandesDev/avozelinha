<script lang="ts">
	import Button from '$lib/components/Button.svelte';
</script>

<form>
	<input type="text" placeholder="O seu nome..." />
	<input type="text" placeholder="O seu contacto..." />
	<textarea placeholder="A sua mensagem..." />
	<Button>Enviar</Button>
</form>

<style>
	textarea,
	input {
		width: 100%;
		margin: 0;
		padding: 0.5rem 0.25rem;
		margin-bottom: var(--mg-sm);
		border: 1px solid #ffffff;
		border-radius: 4px;
		background-color: transparent;
		color: #ffffff;
		font-family: var(--fontType);
	}

	textarea {
		min-height: 70px;
	}

	textarea::placeholder,
	input::placeholder {
		color: #ffffff;
		font-size: 0.9rem;
	}
</style>
