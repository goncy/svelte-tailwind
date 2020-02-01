<script>
  export let color = "blue";

  const variants = {
    blue: "border-blue-500 border-blue-500 hover:border-blue-600 hover:bg-blue-500",
    red: "border-red-500 border-red-500 hover:border-red-600 hover:bg-red-500",
  };
</script>

<button
  class={`w-32 bg-white tracking-wide text-gray-800 font-bold rounded border-0 border-b-2 hover:text-white shadow-md py-2
  px-6 inline-flex items-center ${variants[color]}`}>
  <span class="mx-auto">
    <slot />
  </span>
</button>
