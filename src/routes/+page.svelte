<script>
  import "./app.css";
</script>

<body>
  <section class="flex justify-center h-[80vh]">
    <div class="flex justify-between w-[90%] mt-[15rem]">
      <div class="glassy-div h-[12rem] w-[25%] flex-column justify-center">
        <h2 class="text-center">About Us</h2>
        <img src="/family.jpg" alt="later" />
      </div>
      <div
        class="glassy-div h-[12rem] w-[25%] flex-column justify-center items-center"
      >
        <h2 class="text-center">Our Products</h2>
        <img src="/groceries.jpg" alt="later" />
      </div>
      <div class="glassy-div h-[50%] w-[25%]"></div>
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

  img {
    border-radius: 20px;
  }

  h2 {
    font-size: 1.2rem;
    font-weight: bold;
  }

  .glassy-div {
    background: rgba(255, 255, 255, 0.1); /* White background with opacity */
    border-radius: 15px; /* Rounded corners */
    backdrop-filter: blur(5px); /* Initial blur effect */
    -webkit-backdrop-filter: blur(5px); /* For Safari */
    border: 1px solid rgba(255, 255, 255, 0.3); /* Light white border */
    padding: 1rem 1rem 1rem 2rem; /* Space inside the div */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Adds a subtle shadow */
    transition: all 0.2s ease-out;
  }

  .glassy-div:hover {
    transform: scale(1.03); /* Slightly increase size */
    box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2); /* Increase shadow for depth */
  }
</style>
