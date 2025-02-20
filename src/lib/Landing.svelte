<script>
  import { goto } from '$app/navigation';
  function scrollToElement(address) {
    event.preventDefault(); // Prevent default anchor behavior

    const targetElement = document.getElementById(address);
    if (targetElement) {
      const yOffset = -30; // Offset in pixels
      const y = targetElement.getBoundingClientRect().top + window.pageYOffset + yOffset;
      window.scrollTo({top: y, behavior: 'smooth'});
    }
  }
</script>

<section class="h-[calc(100vh-136px)] flex flex-col items-center">
  <div class="flex flex-col justify-center text-center" data-aos="fade-up">
    <h1 class="heading-landing"><span class="text-[var(--accent-purple)]">Simplifying</span> the Way You Work</h1>
    <div class="text-xl md:text-2xl">Custom AI solutions for your business</div>
    <div class="flex justify-center items-center mt-10">
      <button class="secondary-button landing-button mr-5"  onclick={() => scrollToElement('about')}>Learn More</button>
      <button class="primary-button landing-button" onclick={() => goto('/contact')}>Let's Talk</button>
    </div>
  </div>
</section>

<style>

</style>
