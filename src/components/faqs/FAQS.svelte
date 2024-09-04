<script>
  // your script goes here
  import Button from "../../components/Button.svelte";
  import arrow from "../../assets/images/icon-arrow.svg";
  import { fade } from "svelte/transition";
  const faqs = [
    {
      id: "1",
      question: "What is Bookmark?",
      answer:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt justo eget ultricies fringilla. Nullam nec turpis nec nunc fermentum ultricies. Nullam nec turpis nec nunc fermentum ultricies.",
      showing: false,
    },
    {
      id: "2",
      question: "How can I request a new browser?",
      answer:
        "Vivamus auctor, nunc id ultricies ultricies, nunc odio ultricies nunc, nec ultricies nunc odio nec nunc. Nullam nec turpis nec nunc fermentum ultricies. Nullam nec turpis nec nunc fermentum ultricies.",
      showing: false,
    },
    {
      id: "3",
      question: "Is there a mobile app?",
      answer:
        "Vivamus auctor, nunc id ultricies ultricies, nunc odio ultricies nunc, nec ultricies nunc odio nec nunc. Nullam nec turpis nec nunc fermentum ultricies. Nullam nec turpis nec nunc fermentum ultricies.",
      showing: false,
    },
    {
      id: "4",
      question: "What about other Chromium browsers?",
      answer:
        "Vivamus auctor, nunc id ultricies ultricies, nunc odio ultricies nunc, nec ultricies nunc odio nec nunc. Nullam nec turpis nec nunc fermentum ultricies. Nullam nec turpis nec nunc fermentum ultricies.",
      showing: false,
    },
  ];
</script>

<section id="faqs" class="grid place-items-center gap-4 w-full py-12">
  <div class="grid gap-4 px-6 text-center md:w-3/5">
    <h2
      class="text-xl md:text-2xl lg:text-3xl tracking-wide font-bold text-blue-950 capitalize"
    >
      Frequently Asked Questions
    </h2>
    <p>
      Here are some FAQS. If you have any other questions, you will like us to
      answer please feel free to mail us.
    </p>
  </div>
  <div class="w-4/5 md:w-full grid gap-4 place-items-center">
    {#each faqs as faq, i (faq.id)}
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore a11y-no-static-element-interactions -->
      <div
        class="faq border-t-2 p-4 w-full cursor-pointer"
        class:border-b-2={i === faqs.length - 1}
        on:click={() => (faqs[i].showing = !faqs[i].showing)}
      >
        <div
          class="question flex justify-between items-center transition hover:text-red-500"
        >
          <h4 class="font-medium">{faq.question}</h4>
          <Button buttonType="normal">
            <img src={arrow} alt="Arrow" />
          </Button>
        </div>
        {#if faq.showing}
          <!-- content here -->
          <div class="answer" transition:fade>
            <p>{faq.answer}</p>
          </div>
        {/if}
      </div>
    {/each}
    <Button buttonType="secondary">More Info</Button>
  </div>
</section>
