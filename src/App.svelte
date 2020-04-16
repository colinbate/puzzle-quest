<script>
import Part1 from './Part1.svelte';
</script>

<main>
  <h1>Puzzle Quest</h1>
  <Part1/>
</main>

<style>
  main {
    padding: 1rem;
    margin: 0 auto;
  }

  h1 {
    margin-top: 0;
    text-align: center;
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: 960px;
    }
  }
</style>