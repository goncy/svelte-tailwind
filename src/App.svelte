<script>
  import Alert from "./components/Alert.svelte";
  import Button from "./components/Button.svelte";
  import Card from "./components/Card.svelte";
</script>

<main>
  <Button>Blue</Button>
  <Button color="red">Red</Button>

  <div class="my-4">
    <Card />
  </div>

  <Alert />
</main>
