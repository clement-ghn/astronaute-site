<script>
  import { onMount } from "svelte";
  let astronauts = [];
  
  onMount(async () => {
    const response = await fetch("http://api.open-notify.org/astros.json");
    const data = await response.json();
    astronauts = data.people;
  });
</script>

<section class="astronaut-carousel">
  <h2>Astronautes Actuellement dans l'Espace</h2>
  
  {#if astronauts.length > 0}
    <div class="carousel">
      {#each astronauts as astronaut}
        <div class="astronaut-card">
          <img src="https://via.placeholder.com/150" alt={astronaut.name} /> <!-- Placeholder image, replace it with actual images -->
          <h3>{astronaut.name}</h3>
          <p>{astronaut.craft}</p>
        </div>
      {/each}
    </div>
  {:else}
    <p>Chargement des astronautes...</p>
  {/if}
</section>

<style>
  .astronaut-carousel {
    margin: 40px auto;
    text-align: center;
    background-color: #1a1a2e;
    padding: 20px;
    border-radius: 10px;
    color: white;
  }

  .carousel {
    display: flex;
    justify-content: center;
    overflow-x: scroll;
    padding: 20px;
    gap: 20px;
  }

  .astronaut-card {
    background-color: #333;
    padding: 15px;
    border-radius: 10px;
    width: 150px;
    text-align: center;
  }

  .astronaut-card img {
    width: 100%;
    border-radius: 50%;
  }

  .astronaut-card h3 {
    margin-top: 10px;
    font-size: 1rem;
  }

  .astronaut-card p {
    font-size: 0.8rem;
    color: #aaa;
  }
</style>
