<script lang="ts">
  // your script goes here
  import Button from "./Button.svelte";
  import Logo from "./Logo.svelte";
  import hamburger from "../assets/images/icon-hamburger.svg";
  import close from "../assets/images/icon-close.svg";
  import facebook from "../assets/images/icon-facebook.svg";
  import twitter from "../assets/images/icon-twitter.svg";
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
  let showMobileLinks: boolean = false;
  $: mobileOverlayBackgroundColor = showMobileLinks
    ? "rgba(25, 25, 112, 0.8)"
    : "transparent";
</script>

<header class="flex justify-between items-center px-6 py-8 w-full max-w-5xl m-auto">
  <Logo />
  <nav>
    <ul class="hidden md:flex items-center gap-4">
      {#each links as link (link.title)}
        <li>
          <a
            href={link.link}
            class="uppercase tracking-widest text-sm hover:text-red-500 transition"
            >{link.title}</a
          >
        </li>
      {/each}
      <Button uppercase={true} buttonType="danger">Login</Button>
    </ul>
    <Button buttonType="normal" classes="block md:hidden" on:click={() => (showMobileLinks = true)}>
      <img src={hamburger} alt="hamburger" />
    </Button>
  </nav>

  {#if showMobileLinks}
    <!-- content here -->
    <div
      class="fixed top-0 left-0 z-30 min-w-full h-screen p-5 flex flex-col justify-center items-center"
      style:background-color={mobileOverlayBackgroundColor}
    >
      <div class="absolute top-6 right-6">
        <Button
          buttonType="normal"
          classes="block md:hidden"
          on:click={() => (showMobileLinks = false)}
        >
          <img src={close} alt="close" />
        </Button>
      </div>
      <ul class="grid gap-4 place-items-center w-4/5 h-1/3 mb-6">
        {#each links as link (link.title)}
          <li class="mobileLink">
            <a
              href={link.link}
              class="uppercase tracking-widest text-sm hover:text-red-500 transition"
              >{link.title}</a
            >
          </li>
        {/each}
        <li class="mobileLink">
          <a
            href="/"
            class="uppercase tracking-widest text-sm hover:text-red-500 transition"
            >Login</a
          >
        </li>
      </ul>
      <ul class="flex items-center gap-8">
        <li>
          <img src={facebook} alt="facebook" />
        </li>
        <li>
          <img src={twitter} alt="twitter" />
        </li>
      </ul>
    </div>
  {/if}
</header>

<style>
  .mobileLink {
    @apply border-t border-neutral-50 w-4/5 text-center font-medium text-white;
  }
</style>
