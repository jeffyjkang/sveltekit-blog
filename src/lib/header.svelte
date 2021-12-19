<script lang='ts'>
  import { page } from '$app/stores';
</script>

<header>
  <nav>
    <ul>
      <li>
        <a
          href='/'
          class:active={$page.path === '/'}
        >
          Home
        </a>
      </li>
      <li>
        <a
          href='/about'
          class:active={$page.path === '/about'}
        >
          About
        </a>
      </li>
      <li>
        <a
          href='/blog'
          class:active={$page.path === '/blog'}
        >
          Blog
        </a>
      </li>
    </ul>
  </nav>
</header>

<style>
  header {
    height: 1rem;
    display: flex;
    justify-content: space-between;
  }
  nav {
    border-radius: 1rem;
  }
  ul {
    display: flex;
    justify-content: space-between;
  }
  li {
    list-style-type: none;
    margin: 0 8px;
  }
  a {
    text-decoration: none;
  }
  .active {
    border-bottom: 2px solid orange;
  }
</style>

