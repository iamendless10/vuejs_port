<template>
  <section id="experience-section">
    <div class="timeline-container">
    <p class="intro-paragraph">What I've done so far</p>
    <h1 class="timeline-heading">Work Experience</h1>
    <div class="timeline">
      <div
        class="timeline-item"
        v-for="(item, index) in experiences"
        :key="index"
        :class="[ 
          'timeline-item',
          { 'align-left': index % 2 === 0, 'align-right': index % 2 !== 0, 'visible': item.visible }
        ]"
        ref="timelineItems"
      >
        <div class="timeline-content">
          <div class="timeline-icon">
            <img :src="item.icon" alt="icon" />
          </div>
          <h2 class="position">{{ item.position }}</h2>
          <p class="company">{{ item.company }}</p>
          <span class="date">{{ item.date }}</span>
        </div>
      </div>
    </div>
    <div class="resume-container">
      <a href="https://drive.google.com/drive/folders/1vTIEwmnPUK8QCpHOk2UZ4PrR7GTQUv8C?usp=sharing" 
         class="resume-btn" target="_blank">My Resume</a>
    </div>
  </div>
  </section>
  
</template>

  
  <script>
  export default {
    name: "WorkExperience",
    data() {
      return {
        experiences: [
          {
            position: "Flutter Developer",
            company: "Megha",
            date: "Aug 2023 - Oct 2023",
            icon: require('@/assets/mh.png'),
          },
          {
            position: "Full Stack Developer",
            company: "QuickBus",
            date: "Mar 2024 - July 2024",
            icon: require('@/assets/qb.png'),
          },
          {
            position: "Student Mentor",
            company: "Sri Eshwar College of Engineering",
            date: "Jan 2024 - Present",
            icon: require('@/assets/sec.png'),
          },
          {
            position: "President of CSE(AI-ML)",
            company: "Sri Eshwar College of Engineering",
            date: "Aug 2024 - Present",
            icon: require('@/assets/sec.png'),
          },
        ],
      };
    },
    mounted() {
      this.animateOnScroll(); // Call the animation on scroll function
    },
    methods: {
      animateOnScroll() {
        const options = {
          threshold: 0.1, // Trigger when 10% of the element is visible
        };
        const observer = new IntersectionObserver((entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              entry.target.classList.add("visible"); // Add class when in view
            } else {
              entry.target.classList.remove("visible");
            }
          });
        }, options);
  
        // Observe each timeline item
        this.$refs.timelineItems.forEach((item) => {
          observer.observe(item);
        });
      },
    },
  };
  </script>
  
  <style scoped>
  /* Timeline container */
  html {
  scroll-behavior: smooth;
}

  .timeline-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
  }
  
  .intro-paragraph {
    font-family: 'Montserrat', sans-serif;
    font-size: 16px;
    margin-bottom: 20px; /* Adds some space below the paragraph */
    text-align: center; /* Center the text */
    color: #555; /* Optional: Change the text color */
  }
  
  .timeline-heading {
    font-family: 'Montserrat', sans-serif;
    font-size: 36px;
    font-weight: 800;
    margin-bottom: 30px;
    text-align: center;
  }
  
  /* Timeline */
  .timeline {
    position: relative;
    width: 100%;
    max-width: 700px;
    margin: 0 auto;
    padding: 10px 10px;
    display: flex;
    flex-direction: column;
    align-items: center; /* Align center for icons */
  }
  
  /* Timeline item */
  .timeline-item {
    display: flex;
    justify-content: flex-start;
    position: relative;
    padding: 20px 0;
    width: 100%;
    opacity: 0; /* Initially hidden */
    transform: translateY(30px); /* Initial translation for fade-in effect */
    transition: opacity 1s ease-out, transform 1s ease-in-out; /* Transition for fade-in effect */
  }
  
  /* Make timeline item visible */
  .timeline-item.visible {
    opacity: 1; /* Fully visible */
    transform: translateY(0); /* Reset translation */
  }
  
  .align-left {
    justify-content: flex-start; /* Align to the left */
  }
  
  .align-right {
    justify-content: flex-end; /* Align to the right */
  }
  
  /* Icon styles */
  .timeline-icon {
    width: 60px;
    height: 60px;
    background-color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 20px;
  }
  
  .timeline-icon img {
    width: 60px;
    height: 50px;
    overflow: hidden;
  }
  
  /* Timeline content styles */
  .timeline-content {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    width: 350px;
    text-align: left;
  }
  
  /* Position, Company, and Date styles */
  .position {
    font-family: 'Montserrat', sans-serif;
    font-size: 20px;
    font-weight: 700;
  }
  
  .company {
    font-family: 'Montserrat', sans-serif;
    font-size: 16px;
    font-weight: 500;
    margin-bottom: 10px;
  }
  
  .date {
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    color: #777;
  }
  
  /* Vertical line in the timeline */
  .timeline::before {
    content: '';
    position: absolute;
    left: 50%;
    top: 0;
    bottom: 0;
    width: 4px; /* Increased width */
    background-color: #333;
    transform: translateX(-50%);
  }
  
  /* Resume button */
  .resume-container {
    margin-top: 30px;
  }
  
  .resume-btn {
    background-color: #000;
    color: #fff;
    border: none;
    padding: 12px 24px;
    font-size: 16px;
    font-family: 'Montserrat', sans-serif;
    font-weight: 600;
    border-radius: 10px;
    cursor: pointer;
    transition: background-color 0.3s ease;
    text-decoration: none; /* Remove underline from link */
    display: inline-block; /* Align button properly */
  }
  
  .resume-btn:hover {
    background-color: #333;
  }
  </style>
  