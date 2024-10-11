<template>
    <footer class="footer">
      <div class="footer-content">
        <p class="footer-text">Built with 🧠 by Kayal Ennian A G</p>
        <!-- <div class="social-icons">
          <a href="https://www.linkedin.com/in/kayalennian/" target="_blank" class="social-icon" title="LinkedIn">
            <img src="@/assets/linkedin.png" alt="LinkedIn" />
          </a>
          <a href="https://github.com/iamendless10" target="_blank" class="social-icon" title="GitHub">
            <img src="@/assets/github.png" alt="GitHub" />
          </a>
          <a href="https://x.com/kayalennian" target="_blank" class="social-icon" title="X">
            <img src="@/assets/twitter.png" alt="X" />
          </a>
          <a href="https://instagram.com/iam_ennian_" target="_blank" class="social-icon" title="Instagram">
            <img src="@/assets/instagram.png" alt="Instagram" />
          </a>
        </div> -->
      </div>
      <p class="footer-note">© 2024 Kayal Ennian A G. All rights reserved.</p>
    </footer>
  </template>
  
  <script>
  export default {
    name: "FooterComponent",
  };
  </script>
  
  <style scoped>
  .footer {
    background-color: #282c34; /* Dark background */
    color: white;
    padding: 20px 0; /* Adjust padding as needed */
    text-align: center;
    position: relative;
    width: 100vw; /* Use viewport width */
    left: 50%; /* Position it centrally */
    right: 50%; /* Position it centrally */
    transform: translateX(-50%); /* Center it */
    margin: 0; /* Remove default margin */
    height: 40px;
  }
  
  .footer-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 10px;
  }
  
  .footer-text {
    font-family: "Montserrat", sans-serif;
    font-size: 1 rem;
    font-weight: 600;
    margin: 0;
  }
  
  .social-icons {
    display: flex;
    gap: 20px;
  }
  
  .social-icon img {
    width: 30px;
    transition: transform 0.3s ease;
  }
  
  .social-icon img:hover {
    transform: scale(1.1);
  }
  
  .footer-note {
    font-family: "Montserrat", sans-serif;
    font-size: 0.9rem;
    color: #bbb; /* Lighter color for note */
    margin-top: 10px;
  }
  </style>
  
  <style>
  /* Global styles to ensure no margin or padding on body */
  body {
    margin: 0;
    padding: 0;
    overflow-x: hidden; /* Prevent horizontal scroll */
  }
  
  html {
    width: 100%;
  }
  </style>
  