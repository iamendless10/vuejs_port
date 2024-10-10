<template>
  <div class="split-page">
    <!-- Left Side -->
    <div class="left-side">
      <div class="content">
        <!-- Heading -->
        <h1 class="heading">
          My technical stack includes various <span class="highlight">technologies</span> and <span class="highlight">tools</span>
        </h1>

        <!-- Description -->
        <p class="description">
          Explore the technologies I utilize to drive innovation in my projects.
        </p>

        <!-- Get Connect Button -->
        <a href="https://www.linkedin.com/in/kayalennian">
          <button class="connect-btn">Connect with me!</button>
        </a>
      </div>
    </div>

    <!-- Right Side -->
    <div class="right-side">
      <div class="small-containers">
        <!-- Small Containers with Transition -->
        <div
          class="small-container"
          v-for="(tech, index) in techStack"
          :key="index"
          :style="{ animationDelay: index * 0.1 + 's' }"
        >
          <img :src="tech.src" :alt="tech.alt" />
          <h2 class="tech-name">{{ tech.name }}</h2> <!-- Heading for tech stack -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TechnicalStackComponent",
  data() {
    return {
      techStack: [
        { src: require('../assets/cpp.png'), alt: "Vue.js", name: "C++" },
        { src: require('../assets/java.png'), alt: "React", name: "Java" },
        { src: require('../assets/p.png'), alt: "Node.js", name: "Python" },
        { src: require('../assets/dart.png'), alt: "Python", name: "Dart" },
        { src: require('../assets/js.png'), alt: "Java", name: "JavaScript" },
        { src: require('../assets/png-transparent-postgresql-plain-logo-icon.png'), alt: "MySQL", name: "post" },
        { src: require('../assets/c.png'), alt: "MongoDB", name: "C" },
        { src: require('../assets/r.png'), alt: "Docker", name: "React" },
        { src: require('../assets/vuejs.png'), alt: "AWS", name: "Vue" },
        { src: require('../assets/nextjs.svg'), alt: "Git", name: "Next" },
        { src: require('../assets/nodejs.png'), alt: "Figma", name: "Node" },
        { src: require('../assets/es.png'), alt: "TypeScript", name: "Express" },
        { src: require('../assets/flutter-removebg-preview.png'), alt: "MongoDB", name: "Flutter" },
        { src: require('../assets/k.png'), alt: "Docker", name: "Kotlin" },
        { src: require('../assets/github.png'), alt: "AWS", name: "Vue" },
       
      
      ],
    };
  },
};
</script>

<style scoped>
/* Container to split the page */
.split-page {
  display: flex;
  width: 90%;
  height: 90vh; /* Full height of the viewport */
  margin-top: 2%; /* Remove default margin at the top */
}

/* Left side styling */
.left-side {
  flex: 1; /* Take 50% of the width */
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 40px;
  max-width: 40%;
}

/* Content inside the left side */
.content {
  max-width: 80%; /* Set a max-width to avoid overly wide content */
  text-align: left;
}

/* Heading styling */
.heading {
  font-family: "Montserrat", sans-serif;
  font-size: 36px;
  font-weight: 800;
  color: #333; /* Dark text color */
  margin-bottom: 20px; /* Space below heading */
  line-height: 1.3; /* Line height for the two lines */
}

/* Highlighted text */
.highlight {
  color: #858585;
}

/* Description */
.description {
  font-family: "Montserrat", sans-serif;
  font-size: 16px;
  font-weight: 400;
  color: #555;
  margin-bottom: 30px; /* Space below description */
  word-spacing: 4px;
}

/* Button styling */
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

/* Right side styling */
.right-side {
  flex: 1; /* Take 50% of the width */
  display: flex;
  justify-content: center;
  align-items: center; /* Center vertically */
}

/* Container for small images */
.small-containers {
  display: grid;
  grid-template-columns: repeat(6, 100px); /* 6 columns of 100px */
  grid-template-rows: repeat(auto-fill, 120px); /* Increased height to prevent overflow */
  gap: 20px; /* Space between small containers */
}

/* Each small container */
.small-container {
  width: 100px; /* Width of small container */
  height: 120px; /* Increased height for images */
  border-radius: 10px; /* Slightly rounded corners */
  background-color: white; /* Light background for small containers */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Default shadow */
  opacity: 0; /* Initially hidden for transition effect */
  animation: fadeIn 0.5s forwards; /* Fade in animation */
  text-align: center; /* Center text */
  transition: transform 0.3s, box-shadow 0.3s; /* Smooth transitions */
}

.small-container:hover {
  transform: scale(1.1); /* Slightly grow on hover */
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2); /* Increased shadow on hover */
}

/* Image styling */
.small-container img {
  width: 80%; /* Adjusted width for images */
  height: auto; /* Auto height to maintain aspect ratio */
  object-fit: contain;
}

/* Tech name styling */
.tech-name {
  font-family: "Montserrat", sans-serif;
  font-size: 12px; /* Smaller font size for tech names */
  font-weight: 600;
  color: #333; /* Dark text color */
  margin-top: 8px; /* Space above the tech name */
}

/* Animation keyframes for fade in effect */
@keyframes fadeIn {
  0% {
    opacity: 0; /* Start hidden */
    transform: translateY(10px); /* Slide in from below */
  }
  100% {
    opacity: 1; /* Fully visible */
    transform: translateY(0); /* Original position */
  }
}


</style>
