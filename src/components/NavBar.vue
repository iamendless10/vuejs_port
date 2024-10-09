<template>
  <div class="nav-bar">
    <div class="nav-wrapper">
      <!-- Navigation sections on the left -->
      <nav class="nav-sections-left">
        <ul class="nav-links">
          <li><a href="/section1">Experiences</a></li>
          <li><a href="/section3">Skills</a></li>
          <li><a href="/section4">Projects</a></li>
        </ul>
      </nav>

      <!-- Company Logo in the center -->
      <a href="/" class="logo-link">
        <img src="@/assets/ets.png" alt="Logo" class="logo" />
      </a>

      <!-- Navigation sections on the right -->
      <nav class="nav-sections-right">
        <ul class="nav-links">
          <li><a href="/section4">Projects</a></li>
          <li><a href="/section5">Certificates</a></li>

          <!-- Connect link with a separate oval container -->
          <li><a href="/section7" class="connect-btn">Connect</a></li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
/* General nav-bar styles */
.nav-bar {
  background-color: rgba(400, 400, 400, 0.4); /* Translucent background color */
  padding: 1px 2px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2); /* More pronounced shadow for floating effect */
  display: flex;
  justify-content: center; /* Center the entire nav-wrapper */
  align-items: center; /* Center the navbar vertically */
  position: fixed; /* Fixed position at the top */
  top: 20px; /* Gap between the nav-bar and the top of the viewport */
  left: 50%; /* Center horizontally */
  transform: translateX(-50%); /* Proper horizontal centering */
  width: 65%; /* Width to fit the container nicely in the center */
  z-index: 1000; /* Ensure it stays on top */
  height: 80px; /* Fixed height for navbar */
  border-radius: 40px; /* Oval shape */
  transition: all 0.3s ease-in-out; /* Smooth transition for floating effect */
}

/* Nav wrapper */
.nav-wrapper {
  display: flex;
  align-items: center; /* Center items vertically */
  justify-content: space-between;
  width: 100%; /* Full width */
  padding: 0 20px;
}

/* Company logo */
.logo-link {
  display: flex;
  justify-content: center;
  align-items: center;
  flex: 0.5; /* This helps ensure it's centered */
  text-decoration: none; /* Remove underline from the link */
}

.logo {
  height: 50px; /* Adjust the size as needed */
}

/* Navigation sections on both sides */
.nav-sections-left, .nav-sections-right {
  display: flex;
  flex: 1; /* Ensures equal space on both sides */
  justify-content: center; /* Center the nav items */
  align-items: center; /* Align vertically */
}

.nav-links {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
}

.nav-links li {
  margin-left: 20px; /* Adjust spacing between links */
  margin-right: 20px;
}

.nav-links a {
  text-decoration: none;
  font-family: "Montserrat", sans-serif;
  font-size: 17px;
  font-weight: 700;
  color: #758694; /* Default heading color */
  transition: color 0.6s ease; /* Smooth color transition */
}

.nav-links a:hover {
  color: #1f1f39;  
}

/* Oval container for Connect link */
.connect-link {
  background-color: #1f1f39; /* Slight black color */
  color: white; /* Set text color to white */
  padding: 10px 20px;
  border-radius: 30px; /* Oval shape */
  transition: background-color 0.7s ease, color 0.7s ease;
}

.connect-btn {
    background-color: #000; /* Black button background */
    color: #fff; /* White text */
    border: none;
    padding: 12px 24px;
    font-size: 16px;
    font-family: "Montserrat", sans-serif;
    font-weight: 600;
    border-radius: 30px; /* Rounded button */
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .connect-btn:hover {
    background-color: #333; /* Darker shade on hover */
  }
</style>
