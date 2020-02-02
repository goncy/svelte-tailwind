<script>
  export let title;
  export let image;
</script>

<div class="max-w-xl w-full lg:flex">
  <div
    class="h-48 lg:h-auto lg:w-48 flex-none bg-cover rounded-t lg:rounded-t-none lg:rounded-l text-center
    overflow-hidden"
    style="background-image: url('{image}')"
    title="Woman holding a mug" />
  <div
    class="border-r border-b border-l border-grey-light lg:border-l-0 lg:border-t lg:border-grey-light bg-white
    rounded-b lg:rounded-b-none lg:rounded-r p-4 flex flex-col justify-between leading-normal">
    <div class="mb-8">
      <div class="text-black font-bold text-xl mb-2">{title}</div>
      <p class="text-grey-darker text-base">
        <slot />
      </p>
    </div>
    <div class="flex items-center">
      <img
        class="w-10 h-10 rounded-full mr-4"
        src="https://pbs.twimg.com/profile_images/885868801232961537/b1F6H4KC_400x400.jpg"
        alt="Avatar of Jonathan Reinink" />
      <div class="text-sm">
        <p class="text-black leading-none">Jonathan Reinink</p>
        <p class="text-grey-dark">Aug 18</p>
      </div>
    </div>
  </div>
</div>
