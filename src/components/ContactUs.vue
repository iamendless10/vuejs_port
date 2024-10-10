<template>
    <div class="contact-container">
      <h1 class="contact-heading">Get in Touch</h1>
      <p class="contact-description">
        Have questions or want to connect? Feel free to reach out!
      </p>
      <form @submit.prevent="handleSubmit" class="contact-form">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="name" required />
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" required />
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="message" required></textarea>
        </div>
        <button type="submit" class="submit-button">Send Message</button>
      </form>
      <div class="social-icons">
        <a href="https://github.com/iamendless10" class="icon" target="_blank" @mouseover="animateIcon" @mouseleave="resetIcon">
          <img src="@/assets/github.png" alt="Facebook" />
        </a>
        <a href="https://www.twitter.com/kayalennian" class="icon" target="_blank" @mouseover="animateIcon" @mouseleave="resetIcon">
          <img src="@/assets/twitter.png" alt="Twitter" />
        </a>
        <a href="https://www.linkedin.com/in/kayalennian" class="icon" target="_blank" @mouseover="animateIcon" @mouseleave="resetIcon">
          <img src="@/assets/linkedin.png" alt="LinkedIn" />
        </a>
        <a href="https://www.instagram.com/iam_ennian_" class="icon" target="_blank" @mouseover="animateIcon" @mouseleave="resetIcon">
          <img src="@/assets/instagram.png" alt="Instagram" />
        </a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "ContactUs",
    data() {
      return {
        name: "",
        email: "",
        message: "",
      };
    },
    methods: {
  handleSubmit() {
    // Handle form submission logic (e.g., API call)
    console.log("Form submitted:", { name: this.name, email: this.email, message: this.message });
    // Reset form fields
    this.name = "";
    this.email = "";
    this.message = "";
  },
  animateIcon(event) {
    const icon = event.currentTarget.querySelector('img'); // Use currentTarget to access the correct anchor element
    if (icon) { // Check if the icon is not null
      icon.style.transform = "scale(1.2)";
      icon.style.transition = "transform 0.3s ease";
    }
  },
  resetIcon(event) {
    const icon = event.currentTarget.querySelector('img'); // Use currentTarget to access the correct anchor element
    if (icon) { // Check if the icon is not null
      icon.style.transform = "scale(1)";
    }
  },
},

  };
  </script>
  
  <style scoped>
  .contact-container {
    text-align: center;
    margin: 100px auto;
    max-width: 100%;
    padding: 0 20px;
  }
  
  .contact-heading {
    font-family: "Montserrat", sans-serif;
    font-size: 36px;
    font-weight: 800;
    color: #333;
    margin-bottom: 10px; /* Reduced margin for better alignment */
    text-align: center; /* Changed to center */
  }
  
  .contact-description {
    font-family: "Montserrat", sans-serif;
    max-width: 70%;
    font-size: 16px;
    line-height: 28px;
    color: black;
    margin: 0 auto 50px;
    text-align: center; /* Changed to center */
  }
  
  .contact-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }
  
  .form-group {
    width: 100%;
    max-width: 400px;
    text-align: left;
  }
  
  .form-group label {
    font-family: "Montserrat", sans-serif;
    font-size: 14px;
    color: #555;
    margin-bottom: 5px;
  }
  
  .form-group input,
  .form-group textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 16px;
  }
  
  .submit-button {
    background-color: black; /* Changed to black */
    color: white; /* Changed text color to white */
    padding: 10px 20px;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .submit-button:hover {
    background-color: #333; /* Darker shade for hover effect */
  }
  
  .social-icons {
    margin-top: 20px;
    display: flex;
    justify-content: center;
    gap: 20px;
  }
  
  .icon {
    transition: transform 0.3s ease;
  }
  
  .icon img {
    width: 24px; /* Adjusted icon size */
    height: 24px; /* Ensure consistent size */
    transition: transform 0.3s ease; /* Ensure smooth transition on hover */
  }
  </style>
  