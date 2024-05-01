<script>
    export let data
    console.log(data)
</script>

<article class="flow container">    
<h1>{@html data.post.title}</h1>
<img src="{data.post.featured_image}" alt="{data.post.title}">
<div>{@html data.post.content}</div>
</article>

<style>
.container {
    max-width: 48rem;
}
</style>