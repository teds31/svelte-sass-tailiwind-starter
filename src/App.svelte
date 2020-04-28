<script>
  import Tailwindcss from "./Tailwind.svelte";
  import Lazy from "svelte-lazy";
  let name = "Dude";
</script>

<style lang="scss" type="text/scss">
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    @apply bg-green-400;

    h1 {
      text-transform: uppercase;
      font-size: 4em;
      font-weight: 100;
      @apply text-red-700;
    }
    img {
      margin: auto;
      padding: 2rem 0;
    }
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Nice {name}!</h1>
  <h4>Sass nested along with @apply Tailwindcss styling</h4>
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
  <p>
    Visit
    <a href="https://tailwindcss.com/">TailwindCSS</a>
    to learn more
  </p>
  <Lazy height={300} offset={150}>
    <img
      src="https://i.pinimg.com/474x/22/9d/c1/229dc12559d81fd7122abe283dfd2b8f.jpg"
      alt="cool borat" />
  </Lazy>

</main>
