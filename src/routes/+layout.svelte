<script>
    import '$lib/app.css'
    import Header from '$lib/Header.svelte'
    import MobileHeader from '$lib/MobileHeader.svelte'
    import Footer from '$lib/Footer.svelte'

    let innerWidth

    $: console.log(innerWidth)
  </script>
  
  <svelte:window bind:innerWidth />
  <div class="wrapper">
    {#if innerWidth > 900}
    <Header />
    {:else}
    <MobileHeader />
    {/if}
  
    
    <main class="container">
      <slot />
    </main>
  
    <Footer />
  </div>
  
  <style>
    .wrapper {
      min-height: 100dvh;
      display: grid;
      grid-template-rows: auto 1fr auto;
    }
  
    main {
      width: 100%;
      padding-block: 3rem;
      line-height: 1.5
    }
  
  </style>