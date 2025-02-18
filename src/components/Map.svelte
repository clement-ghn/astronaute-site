<script>
  import "leaflet/dist/leaflet.css";
  import L from "leaflet";
  import { onMount } from "svelte";

  let mapContainer;

  onMount(() => {
    const map = L.map(mapContainer).setView([51.505, -0.09], 2); // Initial coordinates

    L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png").addTo(map);

    L.marker([51.5, -0.09]).addTo(map)
      .bindPopup("<b>Mission Space</b><br>La première mission vers Mars.")
      .openPopup();
  });
</script>

<!-- Container specifically for the map -->
<div class="map-container" bind:this={mapContainer}></div>

<style>
  .map-container {
    width: 100%;
    height: 400px; /* Make sure the map has a fixed height */
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  }
</style>
