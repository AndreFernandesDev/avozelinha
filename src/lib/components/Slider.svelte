<script lang="ts">
	export let items: Array<any>;
	export let start: number = 0;

	import Text from '$lib/components/Text.svelte';
	import ArrowButton from '$lib/icons/ArrowButton.svelte';
	import Flag from '$lib/icons/Flag.svelte';

	$: current = start;

	const handleClick = (type: string, target: EventTarget | null) => {
		if (type === 'next') {
			if (current + 1 === items.length) {
				current = 0;
			} else {
				current++;
			}
		} else if (type === 'previous') {
			if (current === 0) {
				current = items.length - 1;
			} else {
				current--;
			}
		}
	};
</script>

<div id="content">
	<span id="testimonial" /><Text fontSize={'1.1rem'}>"{items[current].description}"</Text>
	<div id="client">
		<Text type="h3">{items[current].title}</Text>
	</div>
	<div id="flag">
		<Flag />
	</div>
</div>
<div id="buttonLeft" on:click={(e) => handleClick('previous', e.target)}>
	<ArrowButton />
</div>
<div id="buttonRight" on:click={(e) => handleClick('next', e.target)}>
	<ArrowButton />
</div>

<style>
	#content {
		width: 100%;
		padding: 0;
		padding-bottom: var(--mg-lg);
		flex-direction: column;
		align-items: left;
		gap: var(--mg-sm);
		text-align: left;
		min-height: 75px;
	}

	#flag {
		position: absolute;
		right: 0;
		bottom: -24px;
	}

	#client {
		position: absolute;
		right: 15%;
		min-width: 125px;
		bottom: -1px;
	}

	#buttonLeft {
		position: absolute;
		bottom: -20px;
		left: 10%;
	}

	#buttonRight {
		position: absolute;
		bottom: -20px;
		left: 25%;
		transform: rotate(-180deg);
	}
</style>
