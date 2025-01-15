<script>
    import Form from './Form.svelte';
    import Saos from "saos";
</script>

<section id="contact" class="h-[100svh] flex flex-col justify-center items-center">
    <Saos animation={"from-top .7s"}>
    <h1 class="heading-1 text-center">Let's Make Your Company Smarter.<br> <a href="/contact" class="underline text-[var(--accent-purple)]">Let's Talk</a></h1>
    </Saos>
    <!-- <Form /> -->
</section>

<style>
  @keyframes -global-from-top {
    0% {
      transform: translateY(-30px);
      opacity: 0;
    }
    100% {
      transform: translateY(0);
      opacity: 1;
    }
  }
</style>