<template>
    <div class="split-page">
      <!-- Left Side (Image) -->
      <div class="left-side">
        <img src="../assets/kayal4.jpg" alt="Kayal Ennian" class="left-image" />
      </div>
  
      <!-- Right Side (Text) -->
      <div class="right-side">
        <div class="content">
          <!-- Heading -->
          <h1 class="heading">
            I am a <span class="highlight">Competitive Programmer</span> and
            <span class="highlight">Tech Enthusiast</span>
          </h1>
  
          <!-- Description Text -->
          <p class="description">
            Vue Dev. | Flutter | UI/UX Dev. | Full-Stack Developer | Python Enthusiast | DL Afficionado | President of CSE(AI&ML) at SECE
          </p>
  
          <!-- Get Connect Buttons -->
          <div class="buttons-container">
            <a href="https://www.linkedin.com/in/kayalennian">
              <button class="connect-btn">View Certifications</button>
            </a>
            <a href="https://www.linkedin.com/in/kayalennian">
              <button class="connect-btn">See Achievements!</button>
            </a>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "MyselfPage",
  };
  </script>
  
  <style scoped>
  /* Container to split the page */
  .split-page {
    display: flex;
    width: 100%;
    height: 100vh; /* Full height of the viewport */
    margin-top: 2%; /* Margin at the top */
  }
  
  /* Left side styling (Image side) */
  .left-side {
    flex: 1; /* Take 50% of the width */
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .left-image {
    width: 100%; /* Image takes the full container width */
    max-width: 600px; /* Limit image size */
    height: auto; /* Maintain aspect ratio */
    border-radius: 0 150px 0 150px; /* Rounded top-right and bottom-left corners */
  }
  
  /* Right side styling (Text side) */
  .right-side {
    flex: 1; /* Take 50% of the width */
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 40px;
  }
  
  /* Content inside the right side */
  .content {
    max-width: 600px; /* Set a max-width to avoid overly wide content */
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
  
  /* Description text */
  .description {
    font-family: "Montserrat", sans-serif;
    font-size: 16px;
    font-weight: 400;
    color: #555;
    margin-bottom: 30px; /* Space below description */
    word-spacing: 4px;
  }
  
  /* Buttons container */
  .buttons-container {
    display: flex;
    gap: 20px; /* Add space between buttons */
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
    border-radius: 10px; /* Rounded button */
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .connect-btn:hover {
    background-color: #333; /* Darker shade on hover */
  }
  </style>
  