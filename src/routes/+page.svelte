<script>
  import Navbar from "../components/Navbar.svelte";
  import Hero from "../components/home/Hero.svelte";
  import Features from "../components/features/Features.svelte";
  import Footer from "../components/Footer.svelte";
  import Extensions from "../components/extensions/Extensions.svelte";
  import FAQS from "../components/faqs/FAQS.svelte";
  import Button from "../components/Button.svelte";
</script>

<Navbar />
<main class="max-w-5xl m-auto grid gap-8">
  <Hero />
  <Features />
  <Extensions />
  <FAQS />
</main>
<div
  id="contact"
  class="grid place-items-center gap-4 w-full py-12 bg-blue-400 text-white"
>
  <div class="grid gap-4 text-center w-[90%] p-4 md:w-2/5">
    <p class="uppercase tracking-widest font-medium text-sm text-white">
      35, 000+ already joined
    </p>
    <h2 class="text-xl md:text-2xl lg:text-3xl tracking-wide font-bold">
      Stay up-to-date with what we are doing.
    </h2>
    <div class="flex justify-between gap-4">
      <input
        type="email"
        placeholder="Enter your email address"
        class="p-3 rounded flex-grow text-black"
      />
      <Button buttonType="danger">Contact Us</Button>
    </div>
  </div>
</div>
<Footer />

<style>
  /* your styles go here */
</style>
