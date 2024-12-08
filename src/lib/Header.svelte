<script>
	import { goto } from '$app/navigation';
	import Hamburger from './Hamburger.svelte';
    function scrollToElement(address) {
      event.preventDefault(); // Prevent default anchor behavior

      const targetElement = document.getElementById(address);
      if (targetElement) {
        targetElement.scrollIntoView({ behavior: 'smooth' });
      }
    }

	let open = $state(false);
  </script>

<header class="flex items-center p-4">
	<div class="flex items-center justify-between space-x-4 w-full max-w-screen-xl mx-auto my-4 px-8">
		<a href="/">
			<img src="/logo_and_name.svg" alt="Craftology Logo" class="min-w-[150px] sm:min-w-[250px] sm:min-h-[30px]">
		</a>
		<nav class="hide flex items-center space-x-8 font-semibold">
			<a href="#case-studies" onclick={() => scrollToElement('case-studies')} class="text-md">CASE STUDIES</a>
			<a href="#blog" onclick={() => scrollToElement('blog')} class="text-md">BLOG</a>
			<a href="#contact" onclick={() => scrollToElement('contact')} class="text-md">CONTACT</a>
			<button class="primary-button" onclick={() => scrollToElement('contact')}>LET'S TALK</button>
		</nav>
		<!-- <div class="sm:hidden  lg:block">fwpeokwfpo</div> -->
		<Hamburger bind:open />
		 <div class="{ open ? 'header-menu' : 'hide2' }">
			 <div class="flex flex-col items-center justify-center h-full">
				<button
				  onclick={() => {
					open = false;
					document.body.style.overflow = 'auto';
					scrollToElement('case-studies');
				  }}
		
				  class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
				  data-aos="fade-right"
				  data-aos-delay="400">
				  CASE STUDIES
				</button>
				<button
		
				   onclick={() => {
					open = false;
					document.body.style.overflow = 'auto';
					scrollToElement('blog');
				  }}
		
				  class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
				  data-aos="fade-right"
				  data-aos-delay="450">
				  BLOG
				</button>
				<button
				  onclick={() => {
					open = false;
					document.body.style.overflow = 'auto';
					scrollToElement('contact');
				  }}
		
				  class="{ open ? 'link text-4xl mb-12 font-semibold' : 'hidden' }"
				  data-aos="fade-right"
				  data-aos-delay="500">
				  CONTACT
				</button>
				<button
				  onclick={() => {
					open = false;
					document.body.style.overflow = 'auto';
					scrollToElement('contact');
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
