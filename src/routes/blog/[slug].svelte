<script context='module' lang='ts'>
  export async function load({page, fetch}) {
    const response = await fetch(
      // url `https://dev.to/api/articles/${page.params.slug}`
    )
    const post = await response.json();
    return {
      props: {
        post
      }
    }
  }
</script>

<script lang='ts'>
  export let post
</script>

<svelte:head>
  <title>{post.title}</title>
</svelte:head>

<article>
  <h1>{post.title}</h1>
  {@html post.body_html}
</article>

