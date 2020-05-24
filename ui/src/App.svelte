<script>
  import router from 'page'
  import Home from './Home.svelte'
  import About from './About.svelte'

  let page

  router('/', () => page = Home)
  router('/about', () => page = About)

  router.start()
</script>

<style global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>

<main>
  <svelte:component this={ page } />
</main>
