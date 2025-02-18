<script>
  let menuItems = ['Astronautes', 'Missions', 'Découvertes', 'Communauté'];
</script>

<header>
  <nav>
    <ul>
      {#each menuItems as item}
        <li><a href="#">{item}</a></li>
      {/each}
       <input type="search" placeholder="Rechercher un astronaute ou une mission..." />
    </ul>
  </nav>
</header>

<style>
  header {
    background-color: #0a0b12;
    padding: 20px;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  nav ul {
    list-style-type: none;
    display: flex;
    gap: 20px;
  }

  nav a {
    text-decoration: none;
    color: white;
    font-weight: bold;
  }

  nav input {
    padding: 5px;
    font-size: 1rem;
    border-radius: 5px;
    border: none;
  }
</style>
