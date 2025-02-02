<script>
  import { goto } from '$app/navigation';
  function scrollToElement(address) {
      event.preventDefault(); // Prevent default anchor behavior

      const targetElement = document.getElementById(address);
      if (targetElement) {
        targetElement.scrollIntoView({ behavior: 'smooth' });
      }
    }
</script>

<section class="h-[calc(100svh-136px)] grid grid-cols-1 lg:grid-cols-2 gap-4">
  <div class="flex flex-col justify-center items-start" data-aos="fade-up">
    <h1 class="heading-1"><span class="text-[var(--accent-purple)]">Simplifying</span> the Way You Work</h1>
    <h2 class="heading-3">Software studio with expertise in genAI, LLMs, and Computer Vision.</h2>
    <p class="mb-6">Process transformation is not easy. In Craftology, we help you identify your exact needs.</p>
    <div class="flex space-x-4">
      <button class="secondary-button" onclick={() => scrollToElement('services')}>Learn More</button>
      <button class="primary-button" onclick={() => goto('/contact')}>Let's Talk</button>
    </div>
  </div>

  <div class="hidden lg:flex justify-center items-center px-16" data-aos="fade-up">
    {#if Math.random() > 0.5}
      <img src="/computer_vision.svg"  alt="Computer Vision" >
    {:else}
      <img src="/llms.svg"  alt="LLMs" >
    {/if}
  </div>
</section>

<style>

</style>
