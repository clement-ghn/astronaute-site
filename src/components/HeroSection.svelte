<script>
  let astronautImage = "/path-to-astronaut-image.jpg"; // Remplace par une image réelle
  let missionImage = "/path-to-mission-image.jpg"; // Remplace par une image réelle
</script>

<section class="hero">
  <div class="hero-content">
    <img src={astronautImage} alt="Astronaute" />
    <h1>Explorez l'univers avec les astronautes</h1>
    <p>Découvrez les missions et les astronautes les plus célèbres de l'histoire spatiale.</p>
    <button>En savoir plus</button>
  </div>
  <img class="mission-image" src={missionImage} alt="Mission Spatiale" />
</section>

<style>
  .hero {
    display: flex;
    justify-content: space-between;
    padding: 40px;
    background-color: #1b1b30;
    color: white;
  }

  .hero-content {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .hero h1 {
    font-size: 2.5rem;
  }

  .hero p {
    font-size: 1.2rem;
  }

  .hero button {
    background-color: #ff6f61;
    border: none;
    padding: 10px;
    color: white;
    font-size: 1rem;
    cursor: pointer;
  }

  .mission-image {
    width: 40%;
    border-radius: 15px;
  }
</style>
