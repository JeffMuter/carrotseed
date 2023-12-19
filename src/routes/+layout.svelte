<script>
  import Navbar from "$lib/Navbar.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<Navbar />

<main class="bg-gray-100">
  <slot />
</main>

<Footer />

<style>
  main {
    background: linear-gradient(0deg, white, rgb(231, 231, 231) 50%);
  }
</style>
