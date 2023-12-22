<script>
  import "./app.css";
</script>

<body>
  <section class="flex justify-center items-center h-[80vh]">
    <div class="glassy-div w-[50%]">
      <img
        class="h-[60%] w-auto"
        src="/carrotseed-logo.webp"
        alt="carrotseed logo"
      />
    </div>
  </section>
</body>

<style>
  body {
    background-image: url("green_farm_field.jpg"); /* Path to your background image */
    background-size: cover; /* Covers the entire window */
    background-position: center; /* Center the image */
    background-repeat: no-repeat; /* Prevents the image from repeating */
    background-attachment: fixed; /* Optional: makes the background fixed during scroll */
    height: 100vh; /* Ensure it covers the full height of the viewport */
    margin: 0; /* Removes default margin */
  }

  .glassy-div {
    background: rgba(255, 255, 255, 0.1); /* White background with opacity */
    border-radius: 15px; /* Rounded corners */
    backdrop-filter: blur(10px); /* Blur effect */
    -webkit-backdrop-filter: blur(10px); /* For Safari */
    border: 1px solid rgba(255, 255, 255, 0.3); /* Light white border */
    padding: 3rem; /* Space inside the div */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Optional: Adds a subtle shadow */
  }
</style>
