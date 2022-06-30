<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Services from '$lib/components/Services.svelte';
	import Testimonials from '$lib/components/Testimonials.svelte';
	import Contact from '$lib/components/Contact.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import OpenHours from '$lib/components/OpenHours.svelte';
	import Map from '$lib/components/Map.svelte';
</script>

<main>
	<Navbar />
	<Hero />
	<OpenHours />
	<Services />
	<Testimonials />
	<Map />
	<Contact />
</main>
<Footer />

<style>
	main {
		width: 100%;
	}
</style>
