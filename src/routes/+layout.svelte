<script>
  import Navbar from "$lib/Navbar.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<Navbar />

<main>
  <slot />
</main>

<Footer />

<style>
  main {
    background: linear-gradient(0deg, white, rgb(218, 218, 218) 100%);
  }
</style>
