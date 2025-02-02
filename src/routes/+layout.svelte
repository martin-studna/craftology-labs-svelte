<script>
	import '../app.css';
	import AOS from 'aos'
	import 'aos/dist/aos.css'
	import { Header, Footer } from '$lib';
	import { onMount } from 'svelte';
	let { children } = $props();
	onMount(() => {
		AOS.init({
			duration: 800,
			once: true
		})
	})
</script>



<Header />
<main class="max-w-screen-xl mx-auto my-4 px-8">
	{@render children()}
</main>
<Footer />

