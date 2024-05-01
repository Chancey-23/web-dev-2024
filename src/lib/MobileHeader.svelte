<script>
    import Hamburger from "$lib/icons/Hamburger.svelte";
    import Close from "$lib/icons/Close.svelte";
    let isOpen = false;

    function toggleMenu() {
        isOpen = !isOpen;
    }
</script>

<header>
    <div class="top">
        <div class="logo">
            <a href="/">
                <img src="/favicon.png" alt="logo" />
            </a>
            <div class="hamburger">
                <button on:click={toggleMenu}>
                    {#if isOpen}
                        <Close />
                    {:else}
                        <Hamburger />
                    {/if}
                </button>
            </div>
        </div>

        {#if isOpen}
            <nav>
                <ul class="flow">
                    <li><a on:click={toggleMenu} href="/">Home</a></li>
                    <li><a on:click={toggleMenu} href="/blog">Blog</a></li>
                    <li>
                        <a on:click={toggleMenu} href="/contact">Contact</a>
                    </li>
                </ul>
            </nav>
        {/if}
    </div>
</header>

<style>
    header {
        display: grid;
        gap: 1.5rem;
        padding: 1.5rem;
        background-color: pink;
    }

    .top {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    nav {
        min-height: 100dvh;
    }

    ul {
        list-style: none;
    }

    li {
        padding-block-end: 0.5rem;
        border-bottom: 1px solid;
    }

    a {
        color: white;
    }
</style>
