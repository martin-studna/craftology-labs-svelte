<script>
    let { open = $bindable() } = $props();

    const openMenu = () => {
        open = !open;
        document.body.style.overflow = open ? 'hidden' : 'auto';
    }
</script>

<button 
    class="hamburger show" 
    onclick={openMenu}
    aria-label="Menu"
    style="z-index: 100;"
>
    <div class="{open ? 'line open' : 'line'}"></div>
    <div class="{open ? 'line open' : 'line'}"></div>
    <div class="{open ? 'line shorter open' : 'line shorter'}"></div>
</button>

<style>
    .hamburger {
        cursor: pointer;
        display: flex;
        flex-direction: column;
        
    }
    .show {
        display: none;
    }

    .line {
        background: black;
        width: 2.1rem;
        height: 4px;
        border-radius: 2.5px;
        margin: 6px 0;
        transform: rotate(0deg);
        transition: 0.35s ease-in-out;
    }
    .shorter {
    width: 60%;
    align-self: flex-end;
    }

    .shorter.open {
    width: 100%;
    }

    .line.open:nth-child(1) {
    transform: translateY(10px) rotate(135deg);
    }

    .line.open:nth-child(2) {
    opacity: 0;
    transform: translateX(-20px);
    }

    .line.open:nth-child(3) {
    transform: translateY(-10px) rotate(-135deg);
    }


    @media (max-width: 1024px) { 
        .show {
            display: block;
        }
    }
</style>