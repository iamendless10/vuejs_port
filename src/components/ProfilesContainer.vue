<template>

  <section id="codin">
    <div class="main-container">
    <!-- First Profile -->
    <div class="small-container fade-in-up" ref="container1" @mouseover="onHover" @mouseleave="onLeave">
      <!-- Logo at the top -->
      <div class="logo-container">
        <img src="@/assets/cclogo.png" alt="Logo" />
      </div>

      <!-- One line paragraph -->
      <p class="description">Rating 1614 | 3 Star </p>

      <!-- View Profile button -->
      <button class="view-profile-btn" @click="goToLink('https://www.codechef.com/users/kayalennian10')">View Profile</button>
    </div>

    <!-- Second Profile -->
    <div class="small-container fade-in-left" ref="container2" @mouseover="onHover" @mouseleave="onLeave">
      <!-- Logo at the top -->
      <div class="logo-container">
        <img src="@/assets/cflogo.png" alt="Logo" />
      </div>

      <!-- One line paragraph -->
      <p class="description">Rating 1210 | Pupil@codeforces</p>

      <!-- View Profile button -->
      <button class="view-profile-btn" @click="goToLink('https://codeforces.com/profile/kayalennian10')">View Profile</button>
    </div>

    <!-- Third Profile -->
    <div class="small-container fade-in-right" ref="container3" @mouseover="onHover" @mouseleave="onLeave">
      <!-- Logo at the top -->
      <div class="logo-container">
        <img src="@/assets/leet.png" alt="Logo" />
      </div>

      <!-- One line paragraph -->
      <p class="description">Rating 1695 | 300 Days Streak</p>

      <!-- View Profile button -->
      <button class="view-profile-btn" @click="goToLink('https://leetcode.com/u/Kayalennian10/')">View Profile</button>
    </div>

    <!-- Fourth Profile -->
    <div class="small-container fade-in-down" ref="container4" @mouseover="onHover" @mouseleave="onLeave">
      <!-- Logo at the top -->
      <div class="logo-container">
        <img src="@/assets/cn.png" alt="Logo" />
      </div>

      <!-- One line paragraph -->
      <p class="description">Rating 2010 | Specialist@codeforces</p>

      <!-- View Profile button -->
      <button class="view-profile-btn" @click="goToLink('https://www.naukri.com/code360/profile/Kayal_Ennian')">View Profile</button>
    </div>
  </div>
  </section>



  
</template>

<script>
export default {
  name: "ProfilesContainer",
  mounted() {
    this.animateOnScroll(); // Call animation on scroll function
  },
  methods: {
    animateOnScroll() {
      const options = {
        threshold: 0.5, // Trigger when 50% of the element is visible
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

      // Observe each container
      this.$refs.container1 && observer.observe(this.$refs.container1);
      this.$refs.container2 && observer.observe(this.$refs.container2);
      this.$refs.container3 && observer.observe(this.$refs.container3);
      this.$refs.container4 && observer.observe(this.$refs.container4);
    },
    goToLink(link) {
      window.open(link, '_blank'); // Open the link in a new tab
    },
    onHover(event) {
      event.currentTarget.classList.add('hover-effect'); // Add hover effect
    },
    onLeave(event) {
      event.currentTarget.classList.remove('hover-effect'); // Remove hover effect
    },
  },
};
</script>

<style scoped>
/* Main container holding all four smaller containers */
/* Main container holding all four smaller containers */
.main-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
  max-width: 83%;
  margin: 0 auto;
  padding: 20px;
}

/* Each small container */
.small-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 220px;
  height: 250px;
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 10px 50px rgba(0, 0, 0, 0.2);
  text-align: center;
  opacity: 0; /* Initially hidden */
  transition: opacity 0.6s ease-out, transform 0.6s ease-out, background-color 0.6s ease, box-shadow 0.6s ease; /* Adjusted transition duration */
}

/* Hover Effect */
.small-container.hover-effect {
  transform: scale(1.05); /* Slight scale up */
  box-shadow: 0 15px 100px rgba(0, 0, 0, 0.3); /* Deeper shadow */
  
}

/* Animation effects */
.small-container.visible {
  opacity: 1; /* Fully visible */
}

.fade-in-up {
  transform: translateY(30px);
  transition: transform 0.8s ease, opacity 0.8s ease;
}

.fade-in-up.visible {
  transform: translateY(0);
}

.fade-in-left {
  transform: translateX(-30px);
  transition: transform 0.9s ease, opacity 1.0s ease;
}

.fade-in-left.visible {
  transform: translateX(0);
}

.fade-in-right {
  transform: translateX(30px);
  transition: transform 0.8s ease, opacity 0.8s ease;
}

.fade-in-right.visible {
  transform: translateX(0);
}

.fade-in-down {
  transform: translateY(-30px);
  transition: transform 1s ease, opacity 1s ease;
}

.fade-in-down.visible {
  transform: translateY(0);
}

/* Logo container */
.logo-container {
  width: 100%;
  height: 100px;
  margin-bottom: 20px;
}

.logo-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 5px;
}

/* One-line description */
.description {
  font-family: "Montserrat", sans-serif;
  font-size: 16px;
  color: black;
  margin-bottom: 20px;
}

/* View Profile button */
.view-profile-btn {
  background-color: #000;
  color: #fff;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  border-radius: 30px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.view-profile-btn:hover {
  background-color: #333;
}

</style>
