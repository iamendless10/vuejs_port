<template>
    <div class="landing-page">
      <p class="collab-text">LET'S BUILD SOMETHING TOGETHER</p>
      <h1 class="greeting">Hi, I'm <span class="name">{{ name }}</span></h1>
      <h2 class="title">
        <span class="animated-text">{{ animatedText }}</span>
        <span class="cursor" v-if="isTyping">|</span>
      </h2>
      <p class="description">
        As a competitive programming enthusiast, I revel in dissecting intricate algorithms and optimizing performance metrics,<br>
        all while architecting dynamic back-end frameworks that drive cutting-edge software innovations.
      </p>
      <div class="social-icons">
        <a href="https://www.linkedin.com/in/kayalennian/" target="_blank" class="social-icon">
          <img src="@/assets/linkedin.png" alt="LinkedIn" />
        </a>
        <a href="https://github.com/iamendless10" target="_blank" class="social-icon">
          <img src="@/assets/github.png" alt="GitHub" />
        </a>
        <a href="https://x.com/kayalennian" target="_blank" class="social-icon">
          <img src="@/assets/twitter.png" alt="X" />
        </a>
        <a href="https://instagram.com/iam_ennian_" target="_blank" class="social-icon">
          <img src="@/assets/instagram.png" alt="Instagram" />
        </a>
      </div>
      <button class="scroll-to-top" v-if="showScroll" @click="scrollToTop">
        ↑
      </button>
    </div>
  </template>
  
  <script>
  export default {
    name: "LandingPage",
    data() {
      return {
        name: "Kayal Ennian A G",
        animatedText: "",
        phrases: [
          "A Full-Stack Developer",
          "A Competitive Programmer",
          "A Tech Enthusiast",
          "An Open Source Contributor"
        ],
        typingIndex: 0,
        phraseIndex: 0,
        isTyping: true,
        showScroll: false, // Control visibility of the scroll button
      };
    },
    methods: {
      typeText() {
        if (this.typingIndex < this.phrases[this.phraseIndex].length) {
          this.animatedText += this.phrases[this.phraseIndex].charAt(this.typingIndex);
          this.typingIndex++;
          setTimeout(this.typeText, 150); // Typing speed
        } else {
          setTimeout(this.eraseText, 1000); // Pause before erasing
        }
      },
      eraseText() {
        if (this.typingIndex > 0) {
          this.animatedText = this.phrases[this.phraseIndex].substring(0, this.typingIndex - 1);
          this.typingIndex--;
          setTimeout(this.eraseText, 100); // Erasing speed
        } else {
          this.phraseIndex = (this.phraseIndex + 1) % this.phrases.length; // Cycle through phrases
          this.isTyping = true; // Start typing the next phrase
          this.typeText(); // Start typing again
        }
      },
      scrollToTop() {
        window.scrollTo({ top: 0, behavior: 'smooth' }); // Scroll to top with smooth behavior
      },
      handleScroll() {
        this.showScroll = window.scrollY > 300; // Show button after scrolling down 300px
      },
    },
    mounted() {
      this.typeText(); // Start typing the first phrase on mount
      window.addEventListener('scroll', this.handleScroll); // Add scroll event listener
    },
    beforeUnmount() { // Updated to beforeUnmount
      window.removeEventListener('scroll', this.handleScroll); // Clean up the event listener
    },
  };
  </script>
  
  <style scoped>
  .landing-page {
    text-align: center;
    background-color: #ffffff;
    height: 100vh; /* Full height of the viewport */
    display: flex; /* Use flexbox to center the content */
    flex-direction: column; /* Align items vertically */
    justify-content: center; /* Center items vertically */
    align-items: center; /* Center items horizontally */
    margin: 0; /* Remove default margin */
  }
  
  .collab-text {
    font-family: "Montserrat", sans-serif;
    font-size: 1.0rem; /* Adjust size as needed */
    font-weight: 500;
    color: #333; /* Change color as needed */
    margin-bottom: 10px; /* Space below the collaboration text */
  }
  
  .greeting {
    font-family: "Montserrat", sans-serif;
    font-size: 3rem;
    font-weight: 800;
    color: #333; /* Dark text color */
    margin-bottom: 20px; /* Space below heading */
    line-height: 1.3; /* Line height for the two lines */
  }
  
  .name {
    color: #858585; /* Change color as needed */
  }
  
  .title {
    font-family: "Montserrat", sans-serif;
    font-size: 2.5rem;
    font-weight: 800;
    color: #333; /* Dark text color */
    margin-bottom: 20px; /* Space below heading */
    line-height: 1.3; /* Line height for the two lines */
  }
  
  .animated-text {
    font-weight: bold;
    color: #333; /* Change color as needed */
  }
  
  .cursor {
    display: inline-block;
    animation: blink 0.7s infinite;
  }
  
  .description {
    font-family: "Montserrat", sans-serif;
    font-size: 1rem; /* Adjusted font size */
    font-weight: 300;
    color: #333; /* Dark text color */
    margin-bottom: 50px; /* Space below heading */
  }
  
  .social-icons {
    display: flex; /* Use flexbox to align icons */
    gap: 25px; /* Space between icons */
  }
  
  .social-icons a {
    display: inline-block; /* Make sure the anchor behaves like a block */
  }
  
  .social-icon img {
    width: 30px; /* Adjust the size of icons as needed */
    transition: transform 0.3s ease; /* Smooth scaling */
  }
  
  .social-icon img:hover {
    transform: scale(1.9); /* Scale icon on hover */
  }
  
  .scroll-to-top {
    position: fixed; /* Fixed position */
    bottom: 20px; /* Space from the bottom */
    right: 20px; /* Space from the right */
    background-color: black; /* Button color */
    color: white; /* Text color */
    border: none; /* No border */
    border-radius: 50%; /* Circular shape */
    width: 50px; /* Button width */
    height: 50px; /* Button height */
    font-size: 24px; /* Font size for the arrow */
    cursor: pointer; /* Cursor style on hover */
    display: flex; /* Flexbox to center text */
    justify-content: center; /* Center text horizontally */
    align-items: center; /* Center text vertically */
    opacity: 0.7; /* Semi-transparent */
    transition: opacity 0.3s; /* Smooth transition for opacity */
  }
  
  .scroll-to-top:hover {
    opacity: 1; /* Fully opaque on hover */
  }
  
  @keyframes blink {
    0%, 100% {
      opacity: 1;
    }
    50% {
      opacity: 0;
    }
  }
  </style>
  