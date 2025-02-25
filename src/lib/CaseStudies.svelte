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
            <h2 class="text-2xl font-bold mb-4">Visitors Counting</h2>
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
            <h2 class="text-2xl font-bold mb-4">Smart E-mail Automation</h2>
            <p class="mb-4">
                Smart Email Automation uses AI to categorize emails (complaints, bookings, low priority), detect sentiment, summarize content, and generate automatic replies. It streamlines email management, saves time, and ensures fast, relevant responses.
            </p>
            
            <!-- <button class="primary-button" on:click={() => goto('/case-studies/demand-forecasting')}>Read more</button> -->
        </div>
        <img src="/email_flow.png" alt="Smart Email Automation" class="w-full h-[300px] object-contain" style="border-radius: 30px; box-shadow: 0px 0px 10px;">
        
    </div>
  </div>
  <div data-aos="fade-up">
    <div class="grid md:grid-cols-2 gap-8 items-center bg-white p-6 mt-12">
        <div>
            <h2 class="text-2xl font-bold mb-4">Product Image Search</h2>
            <p class="mb-4">
                Our client received emails from customers with photos of products they wanted or something similar. To fulfill these requests, they had to manually search their entire database to find matching products. This process was tedious and time-consuming.
            </p>
            <p class="mb-4">
                We developed an AI-powered image search algorithm that compares the customer's product photo with products in the database and finds the closest matches automatically.
            </p>
            <p class="mb-4">
                This solution significantly reduced search time, improving efficiency and streamlining our client's workflow.
            </p>

            <!-- <button class="primary-button" on:click={() => goto('/case-studies/knowledge-base')}>Read more</button> -->
        </div>
        <div class="card card-image" style="background: url('/blog-elastic-influencer.png');"></div>
    </div>
  </div>
</section>

<style>

</style>