<template>
  <div class="gallery-container">
    <h1 class="gallery-heading">Gallery of Achievements</h1>
    <p class="gallery-description">
      A showcase of my accomplishments and memorable events. This gallery highlights significant milestones, awards, and experiences that have shaped my journey. Each image reflects my dedication, hard work, and passion, celebrating the achievements that inspire my future endeavors.
    </p>
    <div class="gallery-grid">
      <!-- Column 1 -->
      <div class="column">
        <div class="small-container container1">
          <img src="@/assets/image1.jpg" />
        </div>
        <div class="long-container">
          <img src="@/assets/image2.jpeg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image3.jpg" />
        </div>
      </div>

      <!-- Column 2 -->
      <div class="column">
        <div class="small-container">
          <img src="@/assets/image4.jpg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image5.jpg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image6.jpg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image7.jpg" />
        </div>
      </div>

      <!-- Column 3 -->
      <div class="column">
        <div class="small-container">
          <img src="@/assets/image8.jpg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image9.png" />
        </div>
        <div class="small-container">
          <img src="@/assets/image10.jpg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image11.jpg" />
        </div>
      </div>

      <!-- Column 4 -->
      <div class="column">
        <div class="long-container">
          <img src="@/assets/image12.jpg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image13.jpg" />
        </div>
        <div class="small-container">
          <img src="@/assets/image14.jpg" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GalleryOfAccomplishments",
};
</script>

<style scoped>
.gallery-container {
  text-align: center; /* Center the container text */
  margin: 100px auto;
  max-width: 100%;
  padding: 0 20px;
}

.gallery-heading {
  font-family: "Montserrat", sans-serif;
  font-size: 36px;
  font-weight: 800;
  color: #333;
  margin-bottom: 20px;
  margin-left: 140px;
  text-align: left; /* Align heading to the left */
}

.gallery-description {
  font-family: "Montserrat", sans-serif;
  max-width: 70%;
  font-size: 16px;
  line-height: 28px;
  color: black;
  margin: 0 auto 50px; /* Center paragraph with bottom margin */
  text-align: left; /* Align description text to the left */
  margin-left: 140px;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px; /* Reduced gap between columns */
  max-width: 89%;
  margin: 0 auto; /* Center the grid */
  margin-left: 120px;
}

.column {
  display: flex;
  flex-direction: column;
  align-items: center; /* Center contents of each column */
  gap: 20px;
}

/* Ensure small and long containers are centered */
.small-container,
.long-container {
  display: flex;
  justify-content: center; /* Center image horizontally */
  align-items: center; /* Center image vertically */
  transition: transform 0.3s ease; /* Add transition for hover effect */
}

.small-container:hover,
.long-container:hover {
  transform: scale(1.05); /* Scale up on hover */
}

.small-container {
  width: 290px;
  height: 240px;
  background-color: #e0e0e0;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
}

.long-container {
  width: 290px;
  height: 510px;
  background-color: #e0e0e0;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
}

.small-container img,
.long-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Optional: Add image and heading styles inside containers */
.small-container::after,
.long-container::after {
  position: absolute;
  bottom: 10px;
  left: 10px;
  color: white;
  font-size: 16px;
  background-color: rgba(0, 0, 0, 0.5);
  padding: 5px;
  border-radius: 5px;
}

p {
  max-width: 70%;
  font-size: 16px;
  line-height: 28px;
  color: black;
  text-align: left; /* Align paragraph text to the left */
}
</style>
