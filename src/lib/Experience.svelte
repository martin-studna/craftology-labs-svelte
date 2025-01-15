<script>
    import Saos from "saos";
</script>

<section class="min-h-[100vh] flex flex-col justify-center mt-72">
    <Saos animation={"from-top 1s"}>
    <h1 class="text-5xl mb-12 text-center">Why We Are The <span class="text-[var(--accent-purple)]">Right</span> Choice?</h1>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-center auto-rows-min">
        <div class="p-2  max-w-xs mx-auto">
            <h2 class="text-2xl">6 years</h2>
            <p class="mt-1">Is how long we are in the industry offering end to end software development.</p>
        </div>
        <div class="p-2  max-w-xs mx-auto">
            <h2 class="text-2xl">4 projects</h2>
            <p class="mt-1">Were delivered to our clients since popularization of large language models in 2022.</p>
        </div>
        <div class="p-2  max-w-xs mx-auto">
            <h2 class="text-2xl">2 models</h2>
            <p class="mt-1">Are currently running on client servers actively saving their time and money.</p>
        </div>
    </div>
    </Saos>
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