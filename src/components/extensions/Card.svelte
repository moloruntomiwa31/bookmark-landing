<script>
  import Button from "../Button.svelte";
  import dots from "../../assets/images/bg-dots.svg";
  //props
  export let title;
  export let description;
  export let image;
  export let buttonText;
  export let id;
  export let index;
</script>

<div
  class="card shadow-xl rounded p-6 w-4/5 md:w-[270px] h-[350px] grid place-content-between"
  style="transform: translateY({index * 50}px)"
>
  <div class="header grid place-items-center text-center space-y-2">
    <img src={image} alt={title} />
    <div class="description">
      <h3 class="font-bold text-blue-950">{title}</h3>
      <p>{description}</p>
    </div>
  </div>
  <img src={dots} alt="Dotted lines" />
  <div class="footer grid place-items-center">
    <Button buttonType="secondary" classes="whitespace-nowrap"
      >{buttonText}</Button
    >
  </div>
</div>

<style>
</style>
