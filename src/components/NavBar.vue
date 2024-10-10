<template>
  <div :class="['nav-bar', { 'hidden': isHidden }]">
    <div class="nav-wrapper">
      <!-- Navigation sections on the left -->
      <nav class="nav-sections-left">
        <ul class="nav-links">
          <li><a href="#experience-section">Experiences</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#coding">Coding Profiles</a></li>
        </ul>
      </nav>

      <!-- Name Heading in the center -->
      <div class="name-heading">
        <h1>KAYAL</h1>
      </div>

      <!-- Navigation sections on the right -->
      <nav class="nav-sections-right">
        <ul class="nav-links">
          <li><a href="#projects">Projects</a></li>
          <li><a href="#certificates">Certificates</a></li>
          <li><a href="https://www.linkedin.com/in/kayalennian" target="_blank" class="connect-btn">Connect</a></li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      isHidden: false,
      lastScrollPosition: 0,
    };
  },
  methods: {
    handleScroll() {
      const currentScrollPosition = window.pageYOffset;

      if (currentScrollPosition > this.lastScrollPosition) {
        // User is scrolling down, hide the navbar
        this.isHidden = true;
      } else {
        // User is scrolling up, show the navbar
        this.isHidden = false;
      }

      // Update the last scroll position
      this.lastScrollPosition = currentScrollPosition;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() { // Use 'beforeUnmount' instead of 'beforeDestroy'
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<style scoped>
/* General nav-bar styles with glass effect */
html {
  scroll-behavior: smooth;
}

.nav-bar {
  background: rgba(255, 255, 255, 0.2); /* Transparent white for glass effect */
  backdrop-filter: blur(10px); /* Blurs the background behind the navbar */
  -webkit-backdrop-filter: blur(10px); /* For Safari support */
  padding: 1px 2px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1); /* Softer shadow for a glassy look */
  border: 1px solid rgba(255, 255, 255, 0.3); /* Light border for definition */
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
  transition: top 0.6s ease; /* Smooth transition for showing/hiding */
}

/* Class to hide the navbar */
.nav-bar.hidden {
  top: -100px; /* Move it off the top of the screen */
}

.nav-wrapper {
  display: flex;
  align-items: center; /* Center items vertically */
  justify-content: space-between;
  width: 100%; /* Full width */
  padding: 0 20px;
}

/* Name Heading */
.name-heading {
  flex: 0.5; /* This helps ensure it's centered */
  display: flex;
  justify-content: center;
  align-items: center;
}

.name-heading h1 {
  font-family: 'Kanit', sans-serif;
  font-size: 40px;
  font-weight: 700;
  color: #333333; /* Slight black color */
  margin: 0;
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

/* Default styles for navigation links */
.nav-links a {
  text-decoration: none;
  font-family: "Montserrat", sans-serif;
  font-size: 17px;
  font-weight: 700;
  color: #758694; /* Default heading color */
  transition: color 0.3s ease, transform 0.3s ease; /* Smooth color and transform transition */
}

/* Hover effect for the links */
.nav-links a:hover {
  color: #1f1f39; /* Change color on hover */
  transform: scale(1.1); /* Slightly scale up the text on hover */
}

/* Styling for the Connect button */
.connect-btn {
  background-color: #000; /* Black button background */
  color: white !important; /* Ensure text color is white */
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  border-radius: 30px; /* Rounded button */
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

/* Hover effect for the Connect button */
.connect-btn:hover {
  background-color: #333; /* Darker shade on hover */
  transform: scale(1.1); /* Slightly enlarge the button on hover */
}

</style>
