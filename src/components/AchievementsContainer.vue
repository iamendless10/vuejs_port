<template>
  <div class="containers-section">
    <h1 class="section-heading">My Notable Projects and Achievements</h1>
    <div class="containers-grid">
      <div class="container-card" v-for="(item, index) in items" :key="index">
        <div class="card-header">
          <img :src="item.icon" alt="icon" class="icon" />
          <h2 class="card-title">{{ item.title }}</h2>
        </div>
        <h3 class="subheading">{{ item.subheading1 }}</h3>
        <h3 class="subheading">{{ item.subheading2 }}</h3>
        <p class="description">{{ item.description }}</p>
        <button class="view-project-btn" @click="openLink(item.githubLink)">
          <img src="../assets/github.png" alt="View Icon" class="view-icon" />
          View Project
        </button>
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
        <button class="view-project-btn" @click="openLink(item.githubLink)">
          <img src="../assets/github.png" alt="View Icon" class="view-icon" />
          View Project
        </button>
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
          icon: require("../assets/badge.png"),
          title: "Top 6 at Smart India Hackathon",
          subheading1: "Cloud and Mobile App",
          subheading2: "Innovative Solutions",
          description: "Recognized for developing a cutting-edge solution during a national hackathon.",
          githubLink: "https://github.com/your-repo-url-1", // Replace with your actual GitHub link
        },
        {
          icon: require("../assets/trophy.png"),
          title: "1st Place in National Agricultural Hackathon",
          subheading1: "AI in Agriculture",
          subheading2: "Machine Learning Innovations",
          description: "Created a machine learning model to enhance agricultural productivity and efficiency.",
          githubLink: "https://github.com/your-repo-url-2", // Replace with your actual GitHub link
        },
        {
          icon: require("../assets/wreath.png"),
          title: "Best Student Researcher 2023",
          subheading1: "SECE Awards",
          subheading2: "Research Excellence",
          description: "Awarded for outstanding research contributions in the field of AI and ML.",
          githubLink: "https://github.com/your-repo-url-3", // Replace with your actual GitHub link
        },
        {
          icon: require("../assets/conference.png"),
          title: "Best Paper at International Conference",
          subheading1: "Cancer Detection",
          subheading2: "Uzbekistan 2023",
          description: "Presented pioneering research on using ML techniques for cancer detection.",
          githubLink: "https://github.com/your-repo-url-4", // Replace with your actual GitHub link
        },
        {
          icon: require("../assets/winner.png"),
          title: "1st Place in National Cancer Hackathon",
          subheading1: "Innovative Cancer Solutions",
          subheading2: "Healthcare Technology",
          description: "Developed a project leveraging AI to improve cancer detection methodologies.",
          githubLink: "https://github.com/your-repo-url-5", // Replace with your actual GitHub link
        },
        {
          icon: require("../assets/king.png"),
          title: "President of CSE (AI & ML) Department",
          subheading1: "Leadership Role",
          subheading2: "Student Leadership",
          description: "Led initiatives to promote AI/ML knowledge and assist students with placement-related skills.",
          githubLink: "https://github.com/your-repo-url-6", // Replace with your actual GitHub link
        },
      ],
      additionalItems: [
        {
          icon: require("../assets/social.png"),
          title: "Open Source Contributor",
          subheading1: "GitHub Projects",
          subheading2: "Community Engagement",
          description: "Contributed to various open-source projects, enhancing collaborative development efforts.",
          githubLink: "https://github.com/your-repo-url-7", // Replace with your actual GitHub link
        },
        {
          icon: require("../assets/first.png"),
          title: "1st Place in Project Expo 2023 & 2024",
          subheading1: "CSE AIML Department",
          subheading2: "Innovation Showcase",
          description: "Showcased innovative projects at the annual expo, receiving top honors for creativity.",
          githubLink: "https://github.com/your-repo-url-8", // Replace with your actual GitHub link
        },
        {
          icon: require("../assets/trophy (1).png"),
          title: "Innovative ML Model for Cancer Detection",
          subheading1: "Startup TN Recognition",
          subheading2: "Research Innovation",
          description: "Pioneered a machine learning model that received recognition for its impact on healthcare.",
          githubLink: "https://github.com/your-repo-url-9", // Replace with your actual GitHub link
        },
        
      ],
    };
  },
  methods: {
    openLink(url) {
      window.open(url, "_blank");
    },
  },
};
</script>

<style scoped>
/* Containers Section */
.containers-section {
  text-align: center;

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
  gap: 100px;
}

/* Additional Grid for the second row */
.additional-grid {
  margin-top: 80px; /* Add space between the two rows */
}

/* Container Card Styles */
/* Container Card Styles */
.container-card {
  background: linear-gradient(135deg, #686d76, #333333); /* Dark gradient */
  color: white; /* White text for contrast */
  width: 350px;
  height: 250px;
  padding: 20px;
  border-radius: 10px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  position: relative;
  overflow: hidden;
  text-align: left; /* Align text to the left */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Default light shadow */
}

/* Hover effect for card */
.container-card:hover {
  transform: scale(1.05) rotate(2deg); /* Slight rotation on hover */
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.7); /* Darker shadow on hover */
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
  bottom: -45px; /* Position below the card */
  left: 50%; /* Center horizontally */
  transform: translateX(-50%); /* Adjust to center */
  padding: 10px 20px;

  
  font-family: "Montserrat", sans-serif; /* Ensure it uses the same font style */
   /* Add a white border */
  border-radius: 10px;
  cursor: pointer;
  transition: bottom 0.3s ease, transform 0.3s ease; /* Animate button appearance */
  border: none;
}

/* Show button on card hover */
.container-card:hover .view-project-btn {
  bottom: 45px; /* Move button into view */
  transform: translateX(-50%) scale(1.1); /* Slightly increase button size */
}

/* Button hover effect */
.view-project-btn:hover {
  background-color: #d0d0d0; /* Light shade on hover for effect */
  transform: scale(1.1); /* Increase size on hover */
}

/* View Project Button Icon */
.view-icon {
  width: 16px; /* Adjust size as needed */
  height: 16px;
  margin-right: 5px; /* Space between icon and text */
  vertical-align: middle; /* Align vertically with text */
}

/* View Project Button */



</style>
