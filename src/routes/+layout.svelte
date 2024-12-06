<script>
	import '../app.css';
	import { Header, Footer } from '$lib';
	let { children } = $props();
</script>



<Header />
<main class="max-w-screen-xl mx-auto my-4 px-8">
	{@render children()}
</main>
<Footer />

