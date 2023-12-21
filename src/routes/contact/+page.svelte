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

<section class="flex pt-[8rem] h-auto">
  <div id="map" class="w-[45%]"></div>

  <!-- TODO - style contact button -->
  <div class="w-[45%]">
    <iframe
      title="contact-form"
      src="https://docs.google.com/forms/d/e/1FAIpQLSd83ShBU4jIFGuRdC8bwVvFvJJgtYYo620pla7US9D0mSwsJA/viewform?embedded=true"
      width="640"
      height="821"
      frameborder="0"
      marginheight="0"
      marginwidth="0">Loading…</iframe
    >
  </div>
</section>

<style>
</style>
