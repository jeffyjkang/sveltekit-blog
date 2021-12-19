<script context='module' lang='ts'>
  export async function load({fetch}) {
    const response = await fetch(
      // url `https://dev.to/api/articles?username=[username]`
    )
    const posts = await response.json();
    return {
      props: {
        posts
      }
    }
  }
</script>

<script lang='ts'>
  export let posts
</script>

<svelte:head>
  <title>Blog</title>
</svelte:head>

<section>
  <h1>Blog</h1>
  <ul>
    {#each posts as post}
      <li>
        <a href={`/blog/${post.id}`}>
          {post.title}
        </a>
      </li>
    {/each}
  </ul>
</section>

