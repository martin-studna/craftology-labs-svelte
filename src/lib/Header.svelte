<script>
    function scrollToElement(event) {
      event.preventDefault(); // Prevent default anchor behavior
      const targetId = event.target.getAttribute('href').substring(1);
      const targetElement = document.getElementById(targetId);
      if (targetElement) {
        targetElement.scrollIntoView({ behavior: 'smooth' });
      }
    }
  </script>

<header class="flex items-center p-4">
	<div class="flex items-center justify-between space-x-4 w-full max-w-screen-xl mx-auto my-4 px-8">
		<a href="/">
			<h1 class="text-4xl text-[var(--accent-purple)]">craftology</h1>
		</a>
		<nav class="flex items-center space-x-8 font-semibold">
			<a href="#case-studies" on:click={scrollToElement} class="text-md">CASE STUDIES</a>
			<a href="#blog" on:click={scrollToElement} class="text-md">BLOG</a>
			<a href="#contact" on:click={scrollToElement} class="text-md">CONTACT</a>
			<button class="primary-button">LET'S TALK</button>
		</nav>
	</div>
</header>