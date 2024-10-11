<template>
    <div class="landing-page">
      <p class="collab-text">LET'S BUILD SOMETHING TOGETHER 🤝</p>
      <h1 class="greeting">Hi, I'm <span class="name">{{ name }}</span> 👋</h1>
      <h2 class="title">
        <span class="animated-text">{{ animatedText }}</span>
        <span class="cursor" v-if="isTyping">|</span>
      </h2>
      <p class="description">
        As a competitive programming enthusiast, I revel in dissecting intricate algorithms and optimizing performance metrics,<br />
        all while architecting dynamic back-end frameworks that drive cutting-edge software innovations.
      </p>
      <div class="social-icons">
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
      </div>
      <button class="scroll-to-top" v-if="showScroll" @click="scrollToTop">↑</button>
  
      <div class="icon-container" @click="toggleCommandPrompt" v-if="!commandPromptVisible">
        <span class="icon heart" title="Click to interact">❤️</span>
      </div>
  
      <div class="command-prompt" v-if="commandPromptVisible">
        <h3 class="command-prompt-title">Try it on your Command Prompt!😁</h3>
        <div class="command-line">
          <span class="command-text">npx kayal</span>
          <button class="copy-button" @click="copyToClipboard">📋 Copy</button>
        </div>
      </div>
  
      <!-- Confirmation message for copying -->
      <div class="copy-confirmation" v-if="copyConfirmed">{{ confirmationMessage }}</div>
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
        showScroll: false,
        commandPromptVisible: false,
        copyConfirmed: false,
        confirmationMessage: "Copied!",
      };
    },
    methods: {
      typeText() {
        if (this.typingIndex < this.phrases[this.phraseIndex].length) {
          this.animatedText += this.phrases[this.phraseIndex].charAt(this.typingIndex);
          this.typingIndex++;
          setTimeout(this.typeText, 150);
        } else {
          setTimeout(this.eraseText, 1000);
        }
      },
      eraseText() {
        if (this.typingIndex > 0) {
          this.animatedText = this.phrases[this.phraseIndex].substring(0, this.typingIndex - 1);
          this.typingIndex--;
          setTimeout(this.eraseText, 100);
        } else {
          this.phraseIndex = (this.phraseIndex + 1) % this.phrases.length;
          this.isTyping = true;
          this.typeText();
        }
      },
      scrollToTop() {
        window.scrollTo({ top: 0, behavior: 'smooth' });
      },
      handleScroll() {
        this.showScroll = window.scrollY > 300;
      },
      toggleCommandPrompt() {
        this.commandPromptVisible = !this.commandPromptVisible;
      },
      copyToClipboard() {
  const commandText = "npx kayal";
  navigator.clipboard.writeText(commandText).then(() => {
    this.copyConfirmed = true; // Show confirmation
    this.commandPromptVisible = false; // Hide command prompt
    setTimeout(() => {
      this.copyConfirmed = false; // Hide confirmation after 1 second
    }, 1000); // Close confirmation after 1 second
  });
},

    },
    mounted() {
      this.typeText();
      window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() {
      window.removeEventListener('scroll', this.handleScroll);
    },
  };
  </script>
  
  <style scoped>
  .landing-page {
    text-align: center;
    background-color: #ffffff;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0;
  }
  
  .collab-text {
    font-family: "Montserrat", sans-serif;
    font-size: 1.0rem;
    font-weight: 500;
    color: #333;
    margin-bottom: 10px;
  }
  
  .greeting {
    font-family: "Montserrat", sans-serif;
    font-size: 3rem;
    font-weight: 800;
    color: #333;
    margin-bottom: 20px;
    line-height: 1.3;
  }
  
  .name {
    color: #858585; /* Change color for emphasis */
  }
  
  .title {
    font-family: "Montserrat", sans-serif;
    font-size: 2.5rem;
    font-weight: 800;
    color: #333;
    margin-bottom: 20px;
    line-height: 1.3;
  }
  
  .animated-text {
    font-weight: bold;
    color: #333;
  }
  
  .cursor {
    display: inline-block;
    animation: blink 0.7s infinite;
  }
  
  .description {
    font-family: "Montserrat", sans-serif;
    font-size: 1rem;
    font-weight: 300;
    color: #333;
    margin-bottom: 50px;
  }
  
  .social-icons {
    display: flex;
    gap: 25px;
  }
  
  .social-icons a {
    display: inline-block;
  }
  
  .social-icon img {
    width: 30px;
    transition: transform 0.3s ease;
  }
  
  .social-icon img:hover {
    transform: scale(1.1);
  }
  
  .scroll-to-top {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: black;
    color: white;
    border: none;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    font-size: 24px;
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0.7;
    transition: opacity 0.3s;
  }
  
  .scroll-to-top:hover {
    opacity: 1;
  }
  
  .icon-container {
    display: flex;
    gap: 20px;
    position: fixed;
    bottom: 20px;
    left: 20px;
    cursor: pointer;
  }
  
  .icon {
    font-size: 2rem; /* Adjust the size of the icons */
    transition: transform 0.3s ease; /* Transition for smooth scaling */
  }
  
  .heart:hover {
    transform: scale(1.5); /* Scale the heart icon on hover */
  }
  
  .command-prompt {
    position: fixed;
    bottom: 80px;
    left: 20px;
    background-color: white;
    color: #333;
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 15px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    z-index: 1000;
    font-family: "Montserrat", sans-serif;
    font-size: 1rem;
    font-weight: 300;
    color: #333;
  }
  
  .command-prompt-title {
    font-size: 1.2rem;
    margin-bottom: 10px;
  }
  
  .command-line {
    display: flex;
    justify-content: space-between;
  }
  
  .command-text {
    font-family: "Courier New", Courier, monospace;
    font-weight: 300;
    font-size: 20px;
  }
  
  .copy-button {
    background-color: black;
    color: white;
    border: none;
    border-radius: 5px;
    padding: 5px 10px;
    cursor: pointer;
    transition: background-color 0.9s;
    font-family: "Montserrat", sans-serif;
    font-weight: 600;
    font-size: 15px;
  }
  
  .copy-button:hover {
    background-color: #333333;
  }
  
  .copy-confirmation {
    position: fixed;
    bottom: 160px;
    left: 20px;
    background-color: black; /* Green background */
    color: white;
    border-radius: 5px;
    padding: 5px 10px;
    transition: opacity 0.5s ease;
    z-index: 1000;
  }
  @keyframes blink {
    0% {
      opacity: 1;
    }
    50% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
  </style>
  