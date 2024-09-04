<script lang="ts">
  import facebook from "../assets/images/icon-facebook.svg";
  import twitter from "../assets/images/icon-twitter.svg";
  import Logo from "./Logo.svelte";

  const links: { title: string; link: string }[] = [
    {
      title: "Features",
      link: "#features",
    },
    {
      title: "FAQS",
      link: "#faqs",
    },
    {
      title: "Contact",
      link: "#contact",
    },
  ];
</script>

<footer
  class="bg-neutral-400 flex flex-col md:flex-row items-center justify-around p-8 gap-10"
>
  <div
    class="w-full md:w-1/2 flex flex-col md:flex-row items-center justify-between gap-10"
  >
    <Logo />
    <ul class="grid md:grid-cols-3 gap-2 text-center">
      {#each links as link (link.title)}
        <li>
          <a
            href={link.link}
            class="uppercase tracking-widest text-xs text-white hover:text-red-500 transition"
            >{link.title}</a
          >
        </li>
      {/each}
    </ul>
  </div>
  <div class="w-full md:w-1/2 flex justify-center md:justify-end">
    <ul class="flex items-center gap-8">
      <li>
        <img src={facebook} alt="facebook" />
      </li>
      <li>
        <img src={twitter} alt="twitter" />
      </li>
    </ul>
  </div>
</footer>

<style>
</style>
