<script>
  import Title from "$lib/title.svelte";
  import "../styles/global.css";
</script>

<header>
  <Title title="Svelte" />
</header>
<main>
  <!-- content -->
  <slot />
</main>
<footer>
  <p>Copyright 2022 Don</p>
</footer>

<style>
  header {
    display: flex;
    justify-content: center;
  }
  main {
    max-width: 800px;
    margin: 20px auto;
  }
  footer {
    text-align: center;
  }
</style>
