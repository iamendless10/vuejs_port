<template>
  <div class="split-page">
    <!-- Left Side -->
    <div class="left-side">
      <div class="content">
        <!-- Heading -->
        <h1 class="heading">
          My projects have been recognized by various <span class="highlight">organizations</span> and <span class="highlight">institutions</span>
        </h1>

        <!-- Lorem Ipsum Text -->
        <p class="description">
          Explore some of the organizations that have recognized my work and projects.
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
          v-for="(image, index) in images"
          :key="index"
          :style="{ animationDelay: index * 0.1 + 's' }"
        >
          <img :src="image.src" :alt="image.alt" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecognitionsContainer",
  data() {
    return {
      images: [
        { src: require('../assets/tn.png'), alt: "Image 1" },
        { src: require('../assets/mou.png'), alt: "Image 2" },
        { src: require('../assets/vuega.png'), alt: "Image 3" },
        { src: require('../assets/karpagam.png'), alt: "Image 4" },
        { src: require('../assets/srm.png'), alt: "Image 5" },
        { src: require('../assets/svce.png'), alt: "Image 6" },
        { src: require('../assets/sece.png'), alt: "Image 7" },
        { src: require('../assets/karpagam.png'), alt: "Image 8" },
        { src: require('../assets/ie.png'), alt: "Image 9" },
        { src: require('../assets/vr.png'), alt: "Image 10" },
        { src: require('../assets/startup.png'), alt: "Image 11" },
        { src: require('../assets/goc.png'), alt: "Image 12" },
        { src: require('../assets/startuptn.png'), alt: "Image 13" },
        { src: require('../assets/mh.png'), alt: "Image 14" },
        { src: require('../assets/gssoc.png'), alt: "Image 15" },
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

/* Lorem ipsum description */
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
  grid-template-columns: repeat(5, 128px); /* 5 columns of 128px */
  grid-template-rows: repeat(3, 112px); /* 6 rows of 112px */
  gap: 30px; /* Space between small containers */
}

/* Each small container */
.small-container {
  width: 128px; /* Width of small container */
  height: 112px; /* Height of small container */
  border-radius: 15px; /* Slightly rounded corners */
  background-color: white; /* Light background for small containers */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Default shadow */
  opacity: 0; /* Initially hidden for transition effect */
  animation: fadeIn 0.5s forwards; /* Fade in animation */
}

.small-container img {
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  object-fit: contain;
}

/* Hover effect for small containers */
.small-container:hover {
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2); /* Increased shadow on hover */
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
