<script>
  import Bookmark from "./Bookmark.svelte";
  import Search from "./Search.svelte";
  import Share from "./Share.svelte";
  import { fade, fly } from "svelte/transition";

  const setOfTabs = [
    {
      id: "1",
      title: "Simple bookmarking",
      component: Bookmark,
    },
    {
      id: "2",
      title: "Speedy searching",
      component: Search,
    },
    {
      id: "3",
      title: "Easy sharing",
      component: Share,
    },
  ];
  let activeTab = setOfTabs[0];
</script>

<section id="features" class="grid place-items-center gap-4 w-full px-6">
  <div class="grid gap-4 text-center md:w-1/3">
    <h2
      class="text-xl md:text-2xl lg:text-3xl tracking-wide font-bold text-blue-950 capitalize"
    >
      Features
    </h2>
    <p>
      Our aim is to make it quick and easy for you to access your favourite
      websites. Your bookmarks sync between your devices so that you can access
      them on the go.
    </p>
  </div>
  <div class="w-full grid gap-4 place-items-center">
    <ul
      class="flex flex-col text-center md:flex-row md:justify-center md:text-left gap-8 border-b-2 w-1/2 my-4"
    >
      {#each setOfTabs as tab (tab.id)}
        <li>
          <button
            class={tab.title === activeTab.title
              ? "border-b-2 border-red-500 pb-2 transition font-bold"
              : "font-medium border-b-2 md:border-b-0 pb-2"}
            on:click={() => (activeTab = tab)}
          >
            {tab.title}
          </button>
        </li>
      {/each}
    </ul>
    <div>
      {#key activeTab.title}
        <div transition:fade={{ duration: 500 }}>
          <svelte:component this={activeTab.component} />
        </div>
      {/key}
    </div>
  </div>
</section>
