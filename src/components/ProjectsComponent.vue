<template>
  <div class="full-image-container">
    <!-- First Image Container -->
    <div class="image-container">
      <img :src="mainImage.src" :alt="mainImage.alt" class="blur-image" />
      <div class="overlay">
        <div class="content">
          <h2 class="heading">
            ONCULUS DETECTA
          </h2>
          <p class="description">
            The AI-driven system analyzes 10,000+ pathological images, identifying cancerous lesions with 85% accuracy and enhancing 
            diagnostic efficiency. This empowers healthcare professionals with timely insights, improving patient care by enabling 30% faster decision-making in 
            diagnosis and treatment.
          </p>
          <div class="social-icons">
            <a target="_blank">
              <img src="@/assets/p.png" alt="LinkedIn" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/f.png" alt="GitHub" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/cpp.png" alt="Twitter" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/dart.png" alt="Instagram" class="icon" />
            </a>
          </div>
          <br />
          <a href="https://github.com/iamendless10/Onculus-detecta-app">
            <button class="view-projects-btn">View Project</button>
          </a>
        </div>
      </div>
    </div>

    <!-- Second Image Container -->
    <div class="image-container">
      <img :src="secondImage.src" :alt="secondImage.alt" class="blur-image" />
      <div class="overlay">
        <div class="content">
          <h2 class="heading">ANIDER (ECO-WATCH)</h2>
          <p class="description">
            Developed a nonlethal animal monitoring and deterrent system that secured 1st place at the National Hackathon hosted by the Tamil Nadu Government, showcasing expertise in sustainable farming and contributing to a greener agricultural future.
          </p>
          <div class="social-icons">
            <a target="_blank">
              <img src="@/assets/p.png" alt="LinkedIn" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/f.png" alt="GitHub" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/dart.png" alt="Instagram" class="icon" />
            </a>
          </div>
          <br />
          <a href="https://github.com/iamendless10/Onculus-detecta-app">
            <button class="view-projects-btn">View Project</button>
          </a>
        </div>
      </div>
    </div>

    <!-- Third Image Container -->
    <div class="image-container">
      <img :src="thirdImage.src" :alt="thirdImage.alt" class="blur-image" />
      <div class="overlay">
        <div class="content">
          <h2 class="heading">FLORA X</h2>
          <p class="description">
            Created an AI-driven botanical app that transformed plant management by providing precise identification, cultivation guidance, and disease diagnosis for over 1,500 plant species.
          </p>
          <div class="social-icons">
            <a target="_blank">
              <img src="@/assets/p.png" alt="LinkedIn" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/f.png" alt="GitHub" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/dart.png" alt="Instagram" class="icon" />
            </a>
          </div>
          <br />
          <a href="https://github.com/iamendless10/Onculus-detecta-app">
            <button class="view-projects-btn">View Project</button>
          </a>
        </div>
      </div>
    </div>

    <!-- Fourth Image Container -->
    <div class="image-container">
      <img :src="fourthImage.src" :alt="fourthImage.alt" class="blur-image" />
      <div class="overlay">
        <div class="content">
          <h2 class="heading">ADHIKAAR</h2>
          <p class="description">
            Integrated advanced reporting tools for real-time insights into contract statuses, improving efficiency. Launched a mobile app for users to access contract information and procurement updates instantly.
          </p>
          <div class="social-icons">
            <a target="_blank">
              <img src="@/assets/nodejs.png" alt="LinkedIn" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/js.png" alt="GitHub" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/dart.png" alt="Instagram" class="icon" />
            </a>
            <a target="_blank">
              <img src="@/assets/react.png" alt="React" class="icon" />
            </a>
          </div>
          <br />
          <a href="https://github.com/iamendless10/Onculus-detecta-app">
            <button class="view-projects-btn">View Project</button>
          </a>
        </div>
      </div>
    </div>

    <!-- Fifth Image Container -->
    <div class="image-container">
      <img :src="fifthImage.src" :alt="fifthImage.alt" class="blur-image" />
      <div class="overlay">
        <div class="content">
          <h2 class="heading">NPM Package kayal</h2>
          <p class="description">
            A personal NPM package showcasing my projects and skills, enabling easy integration of my work into any development environment. Perfect for developers looking to leverage innovative solutions and expertise in AI and ML.
          </p>
          <div class="social-icons">
            <a target="_blank">
              <img src="@/assets/js.png" alt="LinkedIn" class="icon" />
            </a>
          </div>
          <br />
          <a href="https://github.com/iamendless10/Onculus-detecta-app">
            <button class="view-projects-btn">View Project</button>
          </a>
        </div>
      </div>
    </div>

    <!-- Sixth Image Container -->
    <div class="image-container">
      <img :src="sixthImage.src" :alt="sixthImage.alt" class="blur-image" />
      <div class="overlay">
        <div class="content">
          <h2 class="heading">THC - MEDUSA</h2>
          <p class="description">
            An AI-powered medical chatbot using Groq, providing real-time symptom analysis and personalized health advice to empower informed healthcare decisions.
          </p>
          <div class="social-icons">
            <a target="_blank">
              <img src="@/assets/p.png" alt="LinkedIn" class="icon" />
            </a>
          </div>
          <br />
          <a href="https://github.com/iamendless10/Onculus-detecta-app">
            <button class="view-projects-btn">View Project</button>
          </a>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "ProjectsComponent",
  data() {
    return {
      mainImage: {
        src: require('../assets/onculus.jpg'),
        alt: "Onculus Detecta Image"
      },
      secondImage: {
        src: require('../assets/anider.jpg'),
        alt: "Second Project Image"
      },
      thirdImage: {
        src: require('../assets/on.jpg'),
        alt: "Third Project Image"
      },
      fourthImage: {
        src: require('../assets/aadhikar.jpg'),
        alt: "Fourth Project Image"
      },
      fifthImage: {
        src: require('../assets/npm.png'),
        alt: "NPX Package Kayal"
      },
      sixthImage: {
        src: require('../assets/medu.jpg'),
        alt: "Sixth Project Image"
      }
    };
  }
};
</script>

<style scoped>
/* Full Image Container */
.full-image-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center; /* Center horizontally */
  align-items: center; /* Center vertically */
  max-width: 93%;
  gap: 20px; /* Add gap between containers */
  margin: 0 auto; /* Center container itself */
}

/* Image container */
.image-container {
  position: relative;
  max-width: 45%; /* Adjust width to fit two per row */
  width: 30%;
  height: 300px;
  border-radius: 15px;
  overflow: hidden; /* Ensures the border-radius applies to children */
  display: flex;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease; /* Add transition for transform and shadow */
}

/* Hover effect */
.image-container:hover {
  transform: scale(1.05); /* Scale the container on hover */
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5); /* Add shadow effect on hover */
}

/* Overlay */
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.6); /* Semi-transparent background */
  display: flex;
  flex-direction: column;
  justify-content: center; /* Center content vertically */
  align-items: center; /* Center content horizontally */
  opacity: 1; /* Initially hidden */
  transition: opacity 0.3s ease; /* Smooth transition for overlay */
}

/* Show overlay on hover */
.image-container:hover .overlay {
  opacity: 1; /* Show overlay on hover */
}

/* Content inside overlay */
.content {
  text-align: center; /* Center text */
  color: white; /* White text color */
}

/* Heading styles */
.heading {
  font-family: "Montserrat", sans-serif;
  font-size: 24px;
  font-weight: 700;
  color: #fff;
  line-height: 1.2;
  margin-bottom: 10px;
}

/* Description styles */
.description {
  font-family: "Montserrat", sans-serif;
  font-size: 14px;
  font-weight: 400;
  color: #fff;
  margin-bottom: 15px;
  word-spacing: 2px;
  max-width: 100%;
  white-space: normal;
}

/* Button styles */
.view-projects-btn {
  background-color: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  font-size: 14px;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  border-radius: 10px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.view-projects-btn:hover {
  background-color: #333;
}

/* Social icons container */
.social-icons {
  display: flex;
  gap: 10px; /* Space between icons */
}

/* Icon styles */
.social-icons a img {
  width: 24px;
  height: 24px;
}
.social-icons {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-bottom: 10px;
}


/* Blur effect on images */
.blur-image {
  width: 100%;
  height: 100%;
  object-fit: cover; /* Maintain aspect ratio */
  filter: blur(2px); /* Apply blur effect */
  transition: filter 0.3s ease; /* Transition for blur */
}

/* Remove blur effect on hover */
.image-container:hover .blur-image {
  filter: blur(0); /* Remove blur on hover */
}

/* Highlighting */
.highlight {
  display: inline-block;
  width: 20px;
  height: 3px;
  background-color: white; /* White highlight color */
  margin: 2px auto; /* Center highlight */
}
</style>
