<template>
    <div class="technical-stack-container">
      <h2 class="technical-stack-heading">My Technical Stack</h2>
  
      <!-- First Subheading: Competitive Programming -->
      <div class="sub-heading-container">
        <img
          src="../assets/bow.png"
          alt="Competitive Programming Icon"
          class="sub-heading-icon"
        />
        <h3 class="sub-heading">Competitive Programming</h3>
      </div>
  
      <div class="stack-containers">
        <div class="stack-container" v-for="(stack, index) in stacks" :key="index">
          <img :src="stack.logo" alt="Logo" class="stack-logo" />
          <h4 class="stack-name">{{ stack.name }}</h4>
        </div>
      </div>
  
      <!-- New Subheading for Full Stack Development -->
      <div class="sub-heading-container">
        <img
          src="../assets/fsd.png"
          alt="Full Stack Development Icon"
          class="sub-heading-icon"
        />
        <h3 class="sub-heading">Full Stack Development</h3>
      </div>
  
      <div class="stack-containers">
        <div class="stack-container" v-for="(stack, index) in fullStackStacks" :key="index">
          <img :src="stack.logo" alt="Logo" class="stack-logo" />
          <h4 class="stack-name">{{ stack.name }}</h4>
        </div>
      </div>



      <div class="sub-heading-container">
        <img
          src="../assets/mob2.png"
          alt="Full Stack Development Icon"
          class="sub-heading-icon"
        />
        <h3 class="sub-heading">Application Development</h3>
      </div>
  
      <div class="stack-containers">
        <div class="stack-container" v-for="(stack, index) in applicationsstacks" :key="index">
          <img :src="stack.logo" alt="Logo" class="stack-logo" />
          <h4 class="stack-name">{{ stack.name }}</h4>
        </div>
      </div>

    </div>

    
  </template>
  
  <script>
  export default {
    name: "TechnicalStackComponent",
    data() {
      return {
        stacks: [
          { name: "C++", logo: require("../assets/cpp.png") },
          
        ],
        fullStackStacks: [
          { name: "REACT", logo: require("../assets/react.png") }, // Example stack
          { name: "VUE", logo: require("../assets/vue.png") }, // Example stack
          { name: "NODE JS", logo: require("../assets/nodejs.png") }, // Example stack
          { name: "MONGO DB", logo: require("../assets/mongodb.png") }, // Example stack
          { name: "JAVA", logo: require("../assets/java.png") }, // Example stack
          { name: "NEXT JS", logo: require("../assets/nextjs.svg") }, // Example stack
          { name: "JAVASCRIPT", logo: require("../assets/js.png") }, // Example stack
          { name: "TAILWIND", logo: require("../assets/tw2.png") }, // Example stack
          { name: "PYTHON", logo: require("../assets/p.png") }, // Example stack
          { name: "REST API", logo: require("../assets/api.png") }, // Example stack
        ],

        applicationsstacks: [
        { name: "FLUTTER", logo: require("../assets/flutter.png") }, // Example stack
        { name: "DART", logo: require("../assets/dart.png") }, // Example stack
        ]
      };
    },
  };
  </script>
  
  <style scoped>
  .technical-stack-container {
    padding: 20px; /* Padding around the container */
    border-radius: 10px; /* Rounded corners */
    margin: 50px auto; /* Center the container */
    max-width: 90%; /* Maximum width for the container */
    width: 100%; /* Full width */
  }
  
  .technical-stack-heading {
    font-family: "Montserrat", sans-serif;
    font-size: 36px;
    font-weight: 800;
    color: #333; /* Dark text color */
    margin-bottom: 20px; /* Space below heading */
    line-height: 1.3; /* Line height for the two lines */
    text-align: left; /* Align left */
  }
  
  .sub-heading-container {
    display: flex; /* Flex display for horizontal alignment */
    align-items: center; /* Center items vertically */
    justify-content: center; /* Center items horizontally */
    margin-bottom: 20px; /* Space below the sub-heading container */
  }
  
  .sub-heading-icon {
    width: 40px; /* Adjust icon width */
    height: 40px; /* Adjust icon height */
    margin-right: 10px; /* Space between icon and sub-heading */
  }
  
  .sub-heading {
    font-family: "Montserrat", sans-serif;
    font-size: 30px;
    font-weight: 800;
    color: #858585;
    text-align: center; /* Center align text */
  }
  
  .stack-containers {
    display: flex; /* Flex display for horizontal alignment */
    flex-wrap: wrap; /* Allow wrapping for smaller screens */
    gap: 15px; /* Space between containers */
    justify-content: center; /* Center the stack containers */
  }
  
  .stack-container {
    display: flex; /* Flex display */
    align-items: center; /* Center items vertically */
    justify-content: center; /* Center items horizontally */
    width: 250px; /* Fixed width */
    height: 100px; /* Fixed height */
    background-color: white; /* White background */
    border-radius: 12px; /* Rounded corners */
    padding: 24px; /* Adjusted padding similar to p-6 */
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1); /* Shadow effect similar to shadow-xl */
    transition: transform 0.3s ease, box-shadow 0.3s ease; /* Transition for hover effect */
  }
  
  .stack-container:hover {
    transform: scale(1.05); /* Slightly enlarge the container */
    box-shadow: 0 20px 30px rgba(0, 0, 0, 0.2); /* Stronger shadow on hover similar to shadow-xl */
  }
  
  .stack-logo {
    width: 70px; /* Logo width */
    height: 70px; /* Logo height */
    margin-right: 10px; /* Space between logo and stack name */
  }
  
  .stack-name {
    font-family: 'Montserrat', sans-serif; /* Font style */
    font-size: 18px; /* Stack name size */
    color: #333; /* Dark text color */
    margin: 0; /* Remove default margin */
    text-align: center; /* Center align text */
    flex-grow: 1; /* Allow text to take remaining space */
  }
  </style>
  