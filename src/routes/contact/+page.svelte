<script>
  import { onMount } from "svelte";

  let map;

  onMount(() => {
    // Load the Google Maps script
    const script = document.createElement("script");
    script.src = `https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY`;
    script.async = true;
    script.defer = true;
    document.head.appendChild(script);

    script.onload = () => {
      // Initialize the map once the script is loaded
      initMap();
    };
  });

  function initMap() {
    // New York City coordinates
    const nyc = { lat: 40.7128, lng: -74.006 };

    // Map options
    const mapOptions = {
      zoom: 10,
      center: nyc,
    };

    // Creating the map
    // @ts-ignore
    map = new google.maps.Map(document.getElementById("map"), mapOptions);

    // Adding a marker on New York City
    // @ts-ignore
    new google.maps.Marker({
      position: nyc,
      map: map,
    });
  }
</script>

<div id="map"></div>

<style>
  #map {
    height: 500px;
    width: 500px;
  }
</style>
