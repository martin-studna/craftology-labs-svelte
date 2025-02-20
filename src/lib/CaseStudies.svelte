<script>
import { goto } from '$app/navigation';
</script>

<section id="case-studies" class="flex flex-col justify-center mt-72">
  <div data-aos="fade-up">
    <h1  class="text-5xl mb-12">Projects developed. <span class="text-[var(--accent-purple)]">Delivered</span>. Used every day.</h1>
  </div>
  <div data-aos="fade-up">
    <div class="grid md:grid-cols-2 gap-8 items-center bg-white p-6">
        <div>
            <h2 class="text-xl font-bold mb-4">PEOPLE COUNTING. FOR BETTER BUSINESS.</h2>
            <p class="mb-4">
                Our client demanded measuring how visitors behaved within his stores. We helped to answer questions like:
            </p>
            <ul class="list-disc list-inside mb-4">
                <li>What are the busiest days and hours?</li>
                <li>How many customers make a purchase?</li>
                <li>How long do my customers stay in the store?</li>
            </ul>
            <button class="primary-button" on:click={() => goto('/case-studies/people-counting')}>Read more</button>
        </div>
        
        
        <div class="card">
            <video src="/camera_video.mp4" autoplay muted loop playsinline class="w-full h-full object-cover" style="border-radius: 30px;"></video>
        </div>
        
    </div>
  </div>
  <div data-aos="fade-up">
    <!-- Section 2 -->
    <div class="grid md:grid-cols-2 gap-8 items-center bg-white p-6 mt-12">
        <div>
            <h2 class="text-xl font-bold mb-4">ORDER LESS. PROFIT MORE.</h2>
            <p class="mb-4">
                Minimizing stocked items is one of the most important indicators of ecommerce businesses. Our client was fed up depending on guessing how his goods will perform this season.
            </p>
            <p class="mb-4">
                We delivered an AI model that can predict that and even more. It is based on his historical data, current trends, market sentiment, and even the weather.
            </p>
            <button class="primary-button" on:click={() => goto('/case-studies/demand-forecasting')}>Read more</button>
        </div>
        <div class="card card-image" style="background: url('/demand_forecasting.webp');"></div>
        
    </div>
  </div>
  <div data-aos="fade-up">
    <div class="grid md:grid-cols-2 gap-8 items-center bg-white p-6 mt-12">
        <div>
            <h2 class="text-xl font-bold mb-4">CORPORATE APPROVED. AI FOR CUBICLE.</h2>
            <p class="mb-4">
                After some hard time coming up with viable solution for our first corporate client, we decided to flip the tables. Only a few companies allow using things like ChatGPT or other generative AI models. The reason is simple, all the conversations are used on training the next generation model. This could lead to unwanted data leaks and privacy breaches.
            </p>
            <p class="mb-4">
                After some consideration our solution was simple.
            </p>
            <ol class="list-decimal list-inside mb-4">
                <li>We trained open source LLM model on company processes and data.</li>
                <li>We deployed this on server running on intranet in the HQ.</li>
                <li>With collaboration with HR we prepared training how to leverage AI to boost productivity.</li>
            </ol>
            <button class="primary-button" on:click={() => goto('/case-studies/knowledge-base')}>Read more</button>
        </div>
        <div class="card card-image" style="background: url('/interactive_knowledge_base.webp');"></div>
    </div>
  </div>
</section>

<style>

</style>