<script>
  import Navbar from "../components/Navbar.svelte";
  import Hero from "../components/home/Hero.svelte";
  import Features from "../components/features/Features.svelte";
  import Footer from "../components/Footer.svelte";
  import Extensions from "../components/extensions/Extensions.svelte";
</script>

<Navbar />
<main class="max-w-5xl m-auto grid gap-8">
  <Hero />
  <Features />
  <Extensions />
</main>
<Footer />

<style>
  /* your styles go here */
</style>
