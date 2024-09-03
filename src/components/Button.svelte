<script>
  // Props
  export let buttonType;
  export let uppercase = false;
  export let classes = "";

  // Reactive styles based on buttonType
  $: buttonStyles =
    buttonType === "primary"
      ? "shadow bg-neutral-400 p-4 rounded tracking-widest text-sm hover:bg-neutral-100 hover:border-neutral-500 transition hover:border"
      : buttonType === "secondary"
        ? "shadow bg-blue-800 text-white p-4 rounded tracking-widest text-sm hover:bg-transparent hover:border-blue-500 hover:text-blue-500 transition hover:border"
        : buttonType === "danger"
          ? "shadow bg-red-500 text-white p-4 rounded tracking-widest text-sm hover:bg-transparent hover:border-red-500 hover:text-red-500 transition hover:border"
          : buttonType === "normal"
            ? "bg-transparent p-4 rounded tracking-widest text-sm"
            : "shadow bg-red-500 text-white p-4 rounded tracking-widest text-sm hover:bg-transparent hover:border-red-500 hover:text-red-500 transition hover:border";
</script>

<button on:click class:uppercase class="{buttonStyles} {classes}">
  <slot />
</button>

<style>
  .uppercase {
    text-transform: uppercase;
  }
</style>
