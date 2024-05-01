<script>
    import Hero from "$lib/Hero.svelte";
</script>

<Hero/>

<section class="section flow">
    <h2>Questions?</h2>
<div class="boxes">
    
    <div class="flow">
        <img src="2-23-23.png" alt="placeholder">
        <div>
            <h3>Contact me!</h3>
        <div class="subheading"></div>
    </div>
     <p>Complete the form to ask me any question!</p>
     <a href="/contact" class="button">Message</a>
    </div>

    <div class="flow">
        <img src="https://picsum.photos/300?random2" alt="placeholder">
        <div><h3>Contributors</h3>
        <div class="subheading">May 2024</div>
        </div>
     <p>Complete the form to contribute to the event</p>
     <a href="/contact" class="button">Contribute</a>
    </div>
</div>
</section>

<style>
    section{
        padding: 3rem;
        background-color: hsl(34, 92%, 43%);
        border-radius: 1rem;
    }
.boxes {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(14rem, 1fr));
gap: 3rem;
}

.subheading {
    text-transform: uppercase;
    font-size: 0.8rem;
    letter-spacing: 1px;
}

.button {
    display: inline-block;
    padding-inline: 1rem;
}
</style>