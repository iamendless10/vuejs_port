<template>
    <div class="split-page">
      <!-- Left Side -->
      <div class="left-side">
        <div class="content">
          <!-- Heading -->
          <h1 class="heading">Welcome to My World of <span class="highlight">Innovation</span> and <span class="highlight">Creativity!</span></h1>
  
          <!-- Lorem Ipsum Text -->
          <p class="description">
            I am Kayal Ennian A G, passionate about AI and ML technologies. As a leader in my college's CSE (AI & ML) department and President of our AI and ML club, I am dedicated to fostering innovation and knowledge-sharing. My journey includes multiple patents, awards in hackathons, and a commitment to leveraging AI for impactful innovation in technology.
          </p>
  
          <!-- Social Media Icons -->
          <div class="social-icons">
            <a href="https://www.linkedin.com/in/kayalennian" target="_blank">
              <img src="@/assets/linkedin.png" alt="LinkedIn" class="icon" />
            </a>
            <a href="https://www.github.com/iamendless10" target="_blank">
              <img src="@/assets/github.png" alt="GitHub" class="icon" />
            </a>
            <a href="https://twitter.com/kayalennian" target="_blank">
                <img src="@/assets/twitter.png" alt="Twitter" class="icon" />
            </a>
            <a href="https://www.instagram.com/iam_ennian_" target="_blank">
                <img src="@/assets/instagram.png" alt="Instagram" class="icon" />
            </a>
          </div>
  
          <!-- Get Connect Button -->
           <a href="https://www.linkedin.com/in/kayalennian"><button class="connect-btn">Get Connect</button></a>
          
        </div>
      </div>
  
      <!-- Right Side -->
      <div class="right-side">
        <img src="../assets/kayal3.jpg" alt="Placeholder Image" class="right-image" />
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "SplitPage",
  };
  </script>
  
  <style scoped>
  /* Container to split the page */
  .split-page {
    display: flex;
    width: 100%;
    height: 100vh; /* Full height of the viewport */
    margin-top: 2%; /* Remove default margin at the top */
  }
  
  /* Left side styling */
  .left-side {
    flex: 1; /* Take 50% of the width */
  
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 40px;
  }
  
  /* Content inside the left side */
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
  
  /* Lorem ipsum description */
  .description {
    font-family: "Montserrat", sans-serif;
    font-size: 16px;
    font-weight: 400;
    color: #555;
    margin-bottom: 30px; /* Space below description */
    word-spacing: 4px;
  }
  
  /* Social media icons */
  .social-icons {
    display: flex;
    justify-content: flex-start; /* Align to the left */
    gap: 20px; /* Space between icons */
    margin-bottom: 30px; /* Space below icons */
  }
  
  /* Icon styling */
  .social-icons a {
    display: inline-block; /* Ensure icons are inline */
    font-size: 24px;
    color: #555;
    transition: color 0.3s ease;
  }
  
  .social-icons a img {
    width: 30px; /* Set width for custom LinkedIn icon */
    height: 30px; /* Set height for custom LinkedIn icon */
  }
  
  .social-icons a:hover {
    color: #000; /* Change color on hover */
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
    align-items: center;
    
  }
  
  .right-image {
    width: 100%; /* Image takes the full container width */
    max-width: 600px; /* Limit image size */
    height: 800px; /* Keep image aspect ratio */
    border-radius: 10px; /* Slightly rounded corners */
  }
  </style>
