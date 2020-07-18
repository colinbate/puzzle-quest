<main>
  <h1><a href="/">Puzzle Quest</a></h1>
  <slot />
</main>

<style>
  main {
    padding: 1rem;
    background-color: #333;
    border-radius: 0.5rem;
    box-sizing: border-box;
  }

  h1, h1 a {
    margin-top: 0;
    text-align: center;
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
  }

  h1 a:hover {
    text-decoration: none;
  }

  @media (min-width: 640px) {
    main {
      max-width: 640px;
      padding: 1rem 3rem;
      font-size: 1.25rem;
      box-shadow: 0 1rem 1.5rem rgba(0, 0, 0, 0.35), 0 0.25rem 0.33rem rgba(0, 0, 0, 0.25);
    }
  }
</style>