<script>
    import Form from '../../lib/Form.svelte';
    import Saos from "saos";
</script>

<Saos animation={"slide-in-top .7s cubic-bezier(0.35, 0.5, 0.65, 0.95) both"}>
<section class="flex flex-col justify-center items-center">
    <h1 class="heading-1 text-center" style="letter-spacing: 0.05em; ">Get In Touch</h1>
    
    <a class="primary-button" target="_blank" rel="noopener noreferrer" href="https://calendar.app.google/KEfV6ckjCn2ig6Kr6">Book a Free Discovery Call</a>
    <div class="text-center mt-4 text-2xl">Or <br> Send Us an E-mail <br> <a href="mailto:hello@craftology.ai" class="text-[var(--accent-purple)]">hello@craftology.com</a></div>
    <Form />

    <div class="text-center">
        <p class="text-xl font-bold">Headquarters</p>
        <p class="text-xl">Příčná 1892/4</p>
        <p class="text-xl">Prague</p>
        <p class="text-xl">Czechia</p>
    </div>
    <div class="text-center my-4"> 
        <p class="text-xl font-bold">VAT ID</p>
        <p class="text-xl">CZ21518025</p>
    </div>
</section>
</Saos>