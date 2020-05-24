<script>
  import router from 'page'
  import Home from './Home.svelte'
  import About from './About.svelte'

  let page

  router('/', () => page = Home)
  router('/about', () => page = About)

  router.start()
</script>

<nav>
  <a href="/">Home</a>
  <a href="/about">About</a>
</nav>

<main>
  <svelte:component this={ page } />
</main>
