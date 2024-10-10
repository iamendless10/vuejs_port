<template>
  <section id="projects">
    <div class="text-container">
      <h1>Projects.</h1>
      <div class="para-container">
        <p>
          Explore some of my notable projects, showcasing innovations in technology and leadership. These initiatives reflect my commitment to harnessing advanced techniques for impactful solutions in various fields. Join me in discovering how I’ve combined creativity and technical expertise to drive positive change. </p>
      </div>
     
    </div>
  </section>
    
  </template>
  
  <script>
  export default {
    name: "HeadingComponent",
  };
  </script>
  
  <style scoped>
  .text-container {
    font-family: "Montserrat", sans-serif; /* Ensure same font as before */
    max-width: 83%; /* Same width as other containers */
    margin: 20px auto; /* Center the text container */
    padding: 20px; /* Add some padding */
    background-color: #fff; /* White background */
    border-radius: 8px; /* Rounded corners */

  }
  
  .text-container h1 {
    font-family: "Montserrat", sans-serif;
      font-size: 36px;
      font-weight: 800;
      color: #333; /* Dark text color */
      margin-bottom: 20px; /* Space below heading */
      line-height: 1.3; /* Line height for the two lines */
      text-align: left;
  }
  
  
  .para-container p {
    max-width: 70%;
    font-size: 16px;
    line-height: 28px;
    color: black;
    text-align: left; /* Align paragraph text to the left */
    
  }
  </style>
  