<script>
  export let color = "blue";
  export let isActive = false;

  const variants = {
    default: {
      blue: "text-gray-800 border-blue-500 border-blue-500 hover:border-blue-600 hover:bg-blue-500 text-white",
      green: "text-gray-800 border-green-500 border-green-500 hover:border-green-600 hover:bg-green-500 text-white",
      red: "text-gray-800 border-red-500 border-red-500 hover:border-red-600 hover:bg-red-500 text-white",
    },
    active: {
      blue: "text-white border-blue-600 bg-blue-500",
      green: "text-white border-green-600 bg-green-500",
      red: "text-white border-red-600 bg-red-500",
    },
  };
</script>

<button
  {...$$props}
  on:click
  class={`hover:text-white w-32 bg-white tracking-wide font-bold rounded border-0 border-b-2 shadow-md py-2
  px-6 inline-flex items-center ${variants[isActive ? 'active' : 'default'][color]} ${$$props.class}`}>
  <span class="mx-auto">
    <slot />
  </span>
</button>
