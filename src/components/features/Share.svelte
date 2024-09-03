<script>
    // your script goes here
    import Button from "../Button.svelte";
    import share from "../../assets/images/illustration-features-tab-3.svg";
  </script>
  
  <div
    class="hero flex flex-col-reverse gap-12 text-center items-center justify-between max-w-full px-6 md:flex-row-reverse md:text-left"
  >
    <div class="space-y-4 md:w-1/2">
      <h3
        class="text-lg md:text-xl lg:text-2xl tracking-wide font-bold text-blue-950"
      >
        Share your bookmarks
      </h3>
      <p class="font-light">
        Easily share your bookmarks and collections with others. Create a shareable link that you can send at the click of a button.
      </p>
      <div class="hero-button gap-4 flex justify-center md:justify-start">
        <Button buttonType="secondary" classes="font-medium">More Info</Button>
      </div>
    </div>
    <div class="relative md:w-1/2">
      <!-- svelte-ignore a11y-img-redundant-alt -->
      <img src={share} alt="Hero Image" class="z-10" />
      <div
        class="bg-blue-800 w-[300px] md:w-[500px] h-36 md:h-44 rounded-tr-full rounded-br-full absolute -z-10 bottom-[5px] md:bottom-[-10px] md:left-[-180px] left-[-50px]"
      ></div>
    </div>
  </div>
  