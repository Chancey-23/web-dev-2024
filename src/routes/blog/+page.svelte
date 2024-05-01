<script>
    import Post from "$lib/Post.svelte";
  
    export let data;
  
    console.log(data.posts);
  </script>
  
  <h1>Blog</h1>
  <div>
    {#each data.posts as post}
      <Post {post} />
    {/each}
  </div>
  
  <style>
    div {
      display: grid;
      gap: 3rem;
      grid-template-columns: repeat(auto-fit, minmax(14rem, 1fr));
      padding-block: 3rem;
    }
  </style>