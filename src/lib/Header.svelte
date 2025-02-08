<script>
	import { goto } from '$app/navigation';
	import Hamburger from './Hamburger.svelte';
    function scrollToElement(address) {
      event.preventDefault(); // Prevent default anchor behavior

      const targetElement = document.getElementById(address);
      if (targetElement) {
        const yOffset = -30; // Offset in pixels
        const y = targetElement.getBoundingClientRect().top + window.pageYOffset + yOffset;
        window.scrollTo({top: y, behavior: 'smooth'});
      }
    }

	let open = $state(false);
</script>

<header class="flex items-center p-4">
	<div class="flex items-center justify-between space-x-4 w-full max-w-screen-xl mx-auto my-4 px-6">
		<a href="/">
			<img src="/logo_and_name.svg" alt="Craftology Logo" loading="lazy" class="min-w-[180px] min-h-[32px] sm:min-w-[220px] sm:min-h-[40px]">
		</a>
		<nav class="hide flex items-center space-x-8 font-semibold">
			<a href="/#services" onclick={() => {if (window.location.pathname !== '/') {goto('/#services')}; scrollToElement('services')}} class="text-md tracking-wider">SERVICES</a>
			<a href="/#case-studies" onclick={() => {if (window.location.pathname !== '/') {goto('/#case-studies')}; scrollToElement('case-studies')}} class="text-md tracking-wider">CASE STUDIES</a>
			<button class="primary-button tracking-wider" onclick={() => goto('/contact')}>LET'S TALK</button>
		</nav>
		<!-- <div class="sm:hidden  lg:block">fwpeokwfpo</div> -->
		<Hamburger bind:open />
		<div class="{ open ? 'header-menu' : 'hide2' }">
			<div class="flex flex-col items-center justify-center h-full">
				<button
					onclick={() => {
						open = false;
						document.body.style.overflow = 'auto';

						if (window.location.pathname !== '/') {
							goto('/#services');
						}
						scrollToElement('services');
					}}
					class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
					>
					SERVICES
				</button>
				<button
					onclick={() => {
						open = false;
						document.body.style.overflow = 'auto';
						if (window.location.pathname !== '/') {
							goto('/#case-studies');
						}
						scrollToElement('case-studies');
					}}
					class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
					>
					CASE STUDIES
				</button>
				<button
					onclick={() => {
						open = false;
						document.body.style.overflow = 'auto';
						goto('/contact');
					}}
					class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
					>
					LET'S TALK
				</button>
			</div>
		</div>
	</div>
</header>

<style>
	.header-menu {
		position: absolute;
		top: 0;
		right: 0;
		width: 100%;
		height: 100%;
		background-color: white;
		opacity: 0.9;
		overflow: hidden;
		z-index: 10;
	}
	.hide2 {
		display: none;
	}

	@media (max-width: 1024px) { 
		.hide {
			display: none;
		}
	}
</style>
