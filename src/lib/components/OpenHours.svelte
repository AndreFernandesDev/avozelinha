<script lang="ts">
	import Container from '$lib/components/Container.svelte';
	import Text from '$lib/components/Text.svelte';
	import Spacing from '$lib/components/Spacing.svelte';
	import String from '$lib/icons/String.svelte';
	import Dots from '$lib/icons/Dots.svelte';
</script>

<section>
	<Container>
		<div id="content">
			<!-- LEFT -->
			<div class="half hourTitle">
				<Text type="h3" fontType="Chalk" fontSize={'2.5rem'}>Durante toda a semana</Text>
				<Dots />
			</div>
			<!-- RIGHT -->
			<div class="half">
				<!-- MORNING -->
				<div class="time">
					<Text type="h3" fontType="Handy" fontSize={'1.25rem'}>Manha</Text>
					<Spacing spacing={'--mg-sm'} />
					<Text type="h3" fontType="Handy" fontSize={'1.75rem'}>9h - 12h</Text>
				</div>
				<Spacing spacing={'--mg-md'} />
				<!-- AFTERNOON -->
				<div class="time">
					<Text type="h3" fontType="Handy" fontSize={'1.25rem'}>Tarde</Text>
					<Spacing spacing={'--mg-sm'} />
					<Text type="h3" fontType="Handy" fontSize={'1.75rem'}>14h - 19h</Text>
				</div>
			</div>
		</div>
		<Spacing spacing={'--mg-sm'} />
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
		align-items: stretch;
	}

	.time {
		justify-content: center;
	}

	.half {
		width: 50%;
		flex-wrap: wrap;
	}

	.hourTitle {
		flex-wrap: nowrap;
	}

	#decoration {
		position: absolute;
		left: 0;
		bottom: 0px;
		transform: rotate(-180deg);
	}
</style>
