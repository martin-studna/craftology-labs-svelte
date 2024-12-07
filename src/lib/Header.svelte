<script>
	import { goto } from '$app/navigation';
	import Hamburger from './Hamburger.svelte';
    function scrollToElement(event) {
      event.preventDefault(); // Prevent default anchor behavior
      const targetId = event.target.getAttribute('href').substring(1);
      const targetElement = document.getElementById(targetId);
      if (targetElement) {
        targetElement.scrollIntoView({ behavior: 'smooth' });
      }
    }

	let open = $state(false);
  </script>

<header class="flex items-center p-4">
	<div class="flex items-center justify-between space-x-4 w-full max-w-screen-xl mx-auto my-4 px-8">
		<a href="/">
			<img src="/logo_and_name.svg" alt="Craftology Logo" class="min-w-[150px] min-h-[30px] sm:min-w-[250px] sm:min-h-[40px]">
		</a>
		<nav class="hide flex items-center space-x-8 font-semibold">
			<a href="#case-studies" onclick={scrollToElement} class="text-md">CASE STUDIES</a>
			<a href="#blog" onclick={scrollToElement} class="text-md">BLOG</a>
			<a href="#contact" onclick={scrollToElement} class="text-md">CONTACT</a>
			<button class="primary-button">LET'S TALK</button>
		</nav>
		<!-- <div class="sm:hidden  lg:block">fwpeokwfpo</div> -->
		<Hamburger bind:open />
		 <div class="{ open ? 'header-menu' : 'hide2' }">
			 <div class="flex flex-col items-center justify-center h-full">
				<button
				  onclick={() => {
					open = false;
					goto('/');
				  }}
		
				  class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
				  data-aos="fade-right"
				  data-aos-delay="400">
				  CASE STUDIES
				</button>
				<button
		
				   onclick={() => {
					open = false;
					goto('/workshops');
				  }}
		
				  class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
				  data-aos="fade-right"
				  data-aos-delay="450">
				  BLOG
				</button>
				<button
				  onclick={() => {
					open = false;
					goto('/contact');
				  }}
		
				  class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
				  data-aos="fade-right"
				  data-aos-delay="500">
				  CONTACT
				</button>
				<button
				  onclick={() => {
					open = false;
					goto('/faq');
				  }}
		
				  class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
				  data-aos="fade-right"
				  data-aos-delay="550">
				  LET'S TALK
				</button>
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
