<script>
    // your script goes here
    import Card from "./Card.svelte";
  import chrome from "../../assets/images/logo-chrome.svg";
  import firefox from "../../assets/images/logo-firefox.svg";
  import opera from "../../assets/images/logo-opera.svg";
    const cards = [
    {
      id: "1",
      title: "Add to Chrome",
      description: "Minimum version 62",
      buttonText: "Add & Install extension",
      image: chrome,
    },
    {
      id: "2",
      title: "Add to Firefox",
      description: "Minimum version 62",
      buttonText: "Add & Install extension",
      image: firefox,
    },
    {
      id: "3",
      title: "Add to Opera",
      description: "Minimum version 62",
      buttonText: "Add & Install extension",
      image: opera,
    },
  ];
</script>

<section id="extensions" class="grid place-items-center gap-4 w-full px-6">
  <div class="grid gap-4 text-center md:w-2/5">
    <h2
      class="text-xl md:text-2xl lg:text-3xl tracking-wide font-bold text-blue-950 capitalize"
    >
      Download extensions
    </h2>
    <p>
      We've got more browsers in the pipeline. Please do let us know if you've
      got a favourite you'd like us to prioritize.
    </p>
  </div>
  <div class="w-full grid md:grid-cols-3 gap-4 place-items-center">
    {#each cards as card (card.id)}
      <Card {...card} />
    {/each}
  </div>
</section>
