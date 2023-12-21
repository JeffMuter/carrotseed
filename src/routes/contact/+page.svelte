<script>
  import { onMount } from "svelte";

  let map;

  onMount(() => {
    // Load the Google Maps script
    const script = document.createElement("script");
    // TODO: Replace YOUR_API_KEY with your Google Maps API key -> svelte might have a built-in way to do this -> google maps api key needs to be on the url, so im not sure how secure you can really get. Do some digging.
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

//TODO - Add a contact form to this page. EmailJS I've used before, but I
remember it being a bit of a hassle, look into potential new solutions.

<style>
  #map {
    height: 500px;
    width: 500px;
  }
</style>
