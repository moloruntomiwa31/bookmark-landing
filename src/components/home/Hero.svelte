<script>
  import Button from "../../components/Button.svelte";
  import heroImage from "../../assets/images/illustration-hero.svg";
</script>

<section
  class="hero flex flex-col-reverse text-center items-center justify-between max-w-full px-6 md:flex-row md:text-left"
>
  <div class="hero-text space-y-4 md:w-[45%]">
    <h1
      class="text-2xl md:text-3xl lg:text-4xl tracking-wide font-extrabold text-blue-950 capitalize"
    >
      A simple bookmark manager
    </h1>
    <p class="font-light">
      A clean and simple interface to organize your favourite websites. Open a
      new browser tab and see your sites load instantly. Try it for free.
    </p>
    <div class="hero-button gap-4 flex">
      <Button buttonType="secondary" classes="font-medium">Get it on Chrome</Button>
      <Button buttonType="primary" classes="font-medium">Get it on Firefox</Button>
    </div>
  </div>
  <div class="hero-image xl:w-[55%] relative">
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img src={heroImage} alt="Hero Image" class="z-10" />
    <div
      class="bg-blue-800 w-[300px] md:w-[500px] h-36 md:h-44 rounded-tl-full rounded-bl-full absolute -z-10 bottom-[10px] md:bottom-[40px] md:right-[-180px] right-[-25px]"
    ></div>
  </div>
</section>
