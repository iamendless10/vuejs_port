<template>
    <div class="education-container">
      <h2 class="education-heading">Education</h2>
      <div class="small-rectangles">
        <div class="small-rectangle" ref="rectangle1">
          <img src="../assets/edu.png" alt="Icon 1" class="icon" />
          <div class="text-content">
            <h3 class="small-rectangle-heading">SRI ESHWAR COLLEGE OF ENGINEERING</h3>
            <p class="small-rectangle-description">2022-2026 | CGPA: 8.62</p>
            <p class="small-rectangle-description">Bachelors in CSE(Artificial Intelligence & Machine Learning)</p>
          </div>
        </div>
        <div class="small-rectangle" ref="rectangle2">
          <img src="../assets/edu.png" alt="Icon 2" class="icon" />
          <div class="text-content">
            <h3 class="small-rectangle-heading">VANI VIDIYALAYA</h3>
            <p class="small-rectangle-description">2018-2020 | Percentage: 64.6%</p>
            <p class="small-rectangle-description">Standard - 10th (SSLC)</p>
          </div>
        </div>
      </div>
      <div class="small-rectangle centered" ref="rectangle3">
        <img src="../assets/edu.png" alt="Icon 3" class="icon" />
        <div class="text-content">
          <h3 class="small-rectangle-heading">SRI RAGAVENDRA</h3>
          <p class="small-rectangle-description">2020-2022 | Percentage: 84.2%</p>
          <p class="small-rectangle-description">Standard - 10th (HSC)</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "EducationComponent",
    mounted() {
      this.checkVisibility(); // Check visibility on mount
      window.addEventListener("scroll", this.handleScroll);
    },
    beforeUnmount() {
      window.removeEventListener("scroll", this.handleScroll);
    },
    methods: {
      handleScroll() {
        this.checkVisibility();
      },
      checkVisibility() {
        const rectangles = [this.$refs.rectangle1, this.$refs.rectangle2, this.$refs.rectangle3];
  
        rectangles.forEach((rectangle) => {
          if (rectangle) { // Ensure rectangle is not null
            const rect = rectangle.getBoundingClientRect();
            if (rect.top < window.innerHeight && rect.bottom > 0) {
              rectangle.classList.add('visible');
            } else {
              rectangle.classList.remove('visible'); // Optional: remove class if not visible
            }
          }
        });
      },
    },
  };
  </script>
  
  <style scoped>
  .education-container {
    top: 200px;
    width: 83%; /* Full width */
    padding: 20px; /* Padding around the container */
    
    border-radius: 10px; /* Rounded corners */
   
    margin-top: 50px; /* Space above the component */
    margin: 0 auto;
  }
  
  .education-heading {
    font-family: 'Montserrat', sans-serif;
    font-size: 36px;
    font-weight: 800;
    margin-bottom: 30px;
    text-align: center;
  }
  
  /* Container for the small rectangles */
  .small-rectangles {
    display: flex; /* Flex display for horizontal alignment */
    justify-content: space-between; /* Space between the rectangles */
    margin-bottom: 20px; /* Space below the small rectangles */
  }
  
  /* Small rectangle styling */
  .small-rectangle {
    display: flex; /* Flex display */
    align-items: center; /* Center items vertically */
    width: 40%; /* 40% width for small rectangles */
    background-color: white; /* White background */
    border-radius: 8px; /* Rounded corners */
    padding: 10px; /* Padding */
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Shadow effect */
    opacity: 0; /* Start hidden */
    transform: translateY(20px); /* Move down for animation */
    transition: opacity 0.5s ease-out, transform 0.5s ease-out; /* Transition properties */
  }
  
  .small-rectangle.visible {
    opacity: 1; /* Fully visible */
    transform: translateY(0); /* Reset position */
  }
  
  /* Icon styling */
  .icon {
    width: 50px; /* Icon width */
    height: 50px; /* Icon height */
    margin-right: 10px; /* Space between icon and text */
  }
  
  /* Text content styling */
  .text-content {
    flex-grow: 1; /* Allow text content to grow */
  }
  
  /* Small rectangle heading styling */
  .small-rectangle-heading {
    font-family: "Montserrat", sans-serif; /* Font style */
    font-size: 20px; /* Heading size */
    color: #333; /* Dark text color */
    margin: 0; /* Remove default margin */
  }
  
  /* Small rectangle description styling */
  .small-rectangle-description {
    font-family: "Montserrat", sans-serif; /* Font style */
    font-size: 14px; /* Description size */
    color: #555; /* Dark gray text color */
  }
  
  /* Centered small rectangle */
  .centered {
    width: 40%; /* 40% width for centered rectangle */
    margin: 0 auto; /* Center the rectangle */
  }
  </style>
  