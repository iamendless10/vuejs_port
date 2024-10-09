<template>
    <div class="containers-section">
      <h1 class="section-heading">My Notable Projects</h1>
      <div class="containers-grid">
        <div class="container-card" v-for="(item, index) in items" :key="index">
          <div class="card-header">
            <img :src="item.icon" alt="icon" class="icon" />
            <h2 class="card-title">{{ item.title }}</h2>
          </div>
          <h3 class="subheading">{{ item.subheading1 }}</h3>
          <h3 class="subheading">{{ item.subheading2 }}</h3>
          <p class="description">{{ item.description }}</p>
          <button class="view-project-btn">View Project</button> <!-- Added button -->
        </div>
      </div>
      <div class="containers-grid additional-grid">
        <div class="container-card" v-for="(item, index) in additionalItems" :key="index + items.length">
          <div class="card-header">
            <img :src="item.icon" alt="icon" class="icon" />
            <h2 class="card-title">{{ item.title }}</h2>
          </div>
          <h3 class="subheading">{{ item.subheading1 }}</h3>
          <h3 class="subheading">{{ item.subheading2 }}</h3>
          <p class="description">{{ item.description }}</p>
          <button class="view-project-btn">View Project</button> <!-- Added button -->
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "AchievementsContainer",
    data() {
      return {
        items: [
          {
            icon: require("../assets/github.png"),
            title: "Project Alpha",
            subheading1: "Innovative Technology",
            subheading2: "AI Solutions",
            description: "Developed a groundbreaking AI model that optimizes resource allocation in real time.",
          },
          {
            icon: require("../assets/github.png"),
            title: "Project Beta",
            subheading1: "Data Analytics",
            subheading2: "Market Insights",
            description: "Created an analytics dashboard that provides actionable insights for marketing strategies.",
          },
          {
            icon: require("../assets/github.png"),
            title: "Project Gamma",
            subheading1: "Blockchain",
            subheading2: "Secure Transactions",
            description: "Implemented a blockchain solution to enhance transaction security and transparency.",
          },
        ],
        additionalItems: [
          {
            icon: require("../assets/github.png"),
            title: "Project Delta",
            subheading1: "Robotics",
            subheading2: "Automation Solutions",
            description: "Designed a robotic system to automate manufacturing processes.",
          },
          {
            icon: require("../assets/github.png"),
            title: "Project Epsilon",
            subheading1: "Web Development",
            subheading2: "Responsive Design",
            description: "Developed a fully responsive website that enhances user experience.",
          },
          {
            icon: require("../assets/github.png"),
            title: "Project Zeta",
            subheading1: "Cloud Computing",
            subheading2: "Infrastructure as Code",
            description: "Implemented cloud infrastructure management using IaC principles.",
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Containers Section */
  .containers-section {
    text-align: center;
    margin: 40px 0;
    max-width: 93%; /* Set the overall width to 93% */
    margin: 0 auto; /* Center the container */
  }
  
  /* Section Heading */
  .section-heading {
    font-family: "Montserrat", sans-serif;
    font-size: 28px;
    font-weight: 700;
    margin-bottom: 20px;
    color: #fff;
  }
  
  /* Containers Grid */
  .containers-grid {
    display: flex; /* Change to flex for centering */
    justify-content: center; /* Center the cards */
    flex-wrap: wrap; /* Allow wrapping for responsiveness */
    gap: 20px;
  }
  
  /* Additional Grid for the second row */
  .additional-grid {
    margin-top: 40px; /* Add space between the two rows */
  }
  
  /* Container Card Styles */
  .container-card {
    background: linear-gradient(135deg, #272829, #272829); /* Dark gradient */
    color: #fff; /* White text for contrast */
    width: 350px;
    height: 400px;
    padding: 20px;
    border-radius: 10px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    position: relative;
    overflow: hidden;
    text-align: left; /* Align text to the left */
  }
  
  /* Hover effect for card */
  .container-card:hover {
    transform: scale(1.05) rotate(2deg); /* Slight rotation on hover */
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.7);
  }
  
  /* Card Header */
  .card-header {
    display: flex;
    align-items: center;
  }
  
  /* Icon Styles */
  .icon {
    width: 40px; /* Adjust icon size */
    height: 40px;
    margin-right: 10px;
  }
  
  /* Card Title Styles */
  .card-title {
    font-family: "Montserrat", sans-serif;
    font-size: 22px;
    font-weight: 700;
    margin: 0; /* Removed margin to maintain alignment */
  }
  
  /* Subheading Styles */
  .subheading {
    font-family: "Montserrat", sans-serif;
    font-size: 16px;
    font-weight: 500;
    color: #f0f0f0; /* Light gray for visibility */
    margin: 5px 0; /* Maintain margins for readability */
  }
  
  /* Description Styles */
  .description {
    font-family: "Montserrat", sans-serif;
    font-size: 14px;
    font-weight: 400;
    color: #d0d0d0; /* Medium gray for description */
    margin-top: 10px; /* Keep some space above the description */
    word-spacing: 2px;
  }
  
  /* View Project Button */
  .view-project-btn {
    position: absolute;
    bottom: -40px; /* Position below the card */
    left: 50%; /* Center horizontally */
    transform: translateX(-50%); /* Adjust to center */
    padding: 10px 20px;
    background-color: #007bff; /* Button background color */
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: bottom 0.3s ease, transform 0.3s ease; /* Animate button appearance */
  }
  
  /* Show button on card hover */
  .container-card:hover .view-project-btn {
    bottom: 20px; /* Move button into view */
    transform: translateX(-50%) scale(1.1); /* Slightly increase button size */
  }
  
  /* Button hover effect */
  .view-project-btn:hover {
    background-color: #0056b3; /* Darker shade on hover */
    transform: scale(1.1); /* Increase size on hover */
  }
  </style>
  