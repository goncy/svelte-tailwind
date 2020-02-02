<script>
  export let title;
</script>

<div class="bg-orange-100 border-l-4 border-orange-600 text-orange-600 p-4" role="alert">
  {#if title}
    <p class="font-bold">{title}</p>
  {/if}
  <p>
    <slot />
  </p>
</div>
