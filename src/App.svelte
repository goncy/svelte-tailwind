<script>
  import Alert from "./components/Alert.svelte";
  import Button from "./components/Button.svelte";
  import Card from "./components/Card.svelte";

  let filter = null;

  const news = [
    {
      type: "fake",
      title: "Can coffee make you a better developer?",
      image: "https://tailwindcss.com/img/card-left.jpg",
      content:
        "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.",
    },
    {
      type: "real",
      title: "Can you write apps in Svelte?",
      image: "https://tailwindcss.com/img/card-left.jpg",
      content:
        "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.",
    },
  ];

  $: filtered = filter ? news.filter((n) => n.type === filter) : news;
</script>

<main>
  <div class="flex justify-center">
    <Button isActive={!filter} on:click={() => (filter = null)} class="mr-2" color="blue">All</Button>
    <Button isActive={filter === 'real'} on:click={() => (filter = 'real')} class="mr-2" color="green">Real</Button>
    <Button isActive={filter === 'fake'} on:click={() => (filter = 'fake')} color="red">Fake</Button>
  </div>

  <div class="my-4">
    {#each filtered as {title, content, image} (title)}
      <Card {title} {image}>{content}</Card>
    {/each}
  </div>

  <Alert title="Warning">News might be fake, I would double check</Alert>
</main>
