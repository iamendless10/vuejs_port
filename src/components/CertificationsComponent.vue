<template>
  <div class="certifications-container">
    <h1 class="certifications-heading">Certifications</h1>
    <p class="certifications-description">List of certifications and their details</p>
    
    <table class="certifications-table">
      <thead>
        <tr>
          <th>Domain</th>
          <th>Certification</th>
          <th>Issuing Organization</th>
          <th>Issue Date</th>
          <th>Credential URL</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(cert, index) in certifications" :key="index">
          <td>{{ cert.domain }}</td>
          <td>{{ cert.certification }}</td>
          <td>{{ cert.issuingOrganization }}</td>
          <td>{{ cert.issueDate }}</td>
          <td>
            <a :href="cert.credentialUrl" target="_blank" aria-label="View {{ cert.certification }} credential">
              {{ cert.credentialUrl ? "Credential Link" : "No Link Available" }}
            </a>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "CertificationsComponent",
  data() {
    return {
      certifications: [
        { domain: "Python", certification: "Advanced Diploma in python programming ADPP", issuingOrganization: "CSC", issueDate: "Mar 2022", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },

        { domain: "HTML & CSS", certification: "Webdeveloper Bootcamp", issuingOrganization: "Udemy", issueDate: "Oct 2022", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "RestAPI", certification: "BackEnd RestAPI Mastery", issuingOrganization: "Udemy", issueDate: "Sep 2023", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "Machine Learning", certification: "Supervised Machine Learning", issuingOrganization: "Stanford University", issueDate: "Aug 2023", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "Algorithms", certification: "Deep Dive into Algorithm Design Paradigms", issuingOrganization: "Udemy", issueDate: "Feb 2023", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "Django", certification: "Python and Django Full Stack Web Developer Bootcamp", issuingOrganization: "Udemy", issueDate: "Mar 2024", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "Java", certification: "Core Java mastery", issuingOrganization: "Scaler", issueDate: "Dec 2023", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "Web Development", certification: "React, NodeJS, Express & MongoDB - The MERN Fullstack Guide", issuingOrganization: "Udemy", issueDate: "Mar 2024", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "Reactjs", certification: "React JS Masterclass", issuingOrganization: "Udemy", issueDate: "Apr 2024", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "Android Application", certification: "The Complete Flutter and Dart Guide", issuingOrganization: "Udemy", issueDate: "Apr 2024", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        // Add more certifications here...
        { domain: "Data Structures", certification: "Mastering Data Structures & Algorithms using C and C++", issuingOrganization: "Udemy", issueDate: "May 2024", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },
        { domain: "DSA", certification: "C++ Data Structures & Algorithms", issuingOrganization: "Udemy", issueDate: "Apr 2024", credentialUrl: "https://drive.google.com/drive/u/1/folders/1Gi7QVixGaIcKeWh6s6jcOt9ngGIccbjI" },

      ]
    };
  }
};
</script>

<style scoped>
.certifications-container {
  color: black; /* Changed to black for better contrast */
  background-color: #f8f9fa; /* Light background color */
  padding: 20px;
  border-radius: 8px;
  margin: 100px auto; /* Center the container */
  width: 93%;
  text-align: center; /* Center-align text */
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1); /* Add shadow to the container */
}

.certifications-heading {
  font-family: "Montserrat", sans-serif;
  font-size: 36px;
  font-weight: 800;
  color: #333; /* Dark text color */
  margin-bottom: 20px; /* Space below heading */
  line-height: 1.3; /* Line height for the two lines */
}

.certifications-description {
  font-size: 1rem; /* Use the same font size as the previous paragraphs */
  margin-bottom: 20px; /* Space below the paragraph */
  font-family: "Montserrat", sans-serif;
  color: #333;
  font-weight: 800;
}

.certifications-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Add shadow to the table */
  border-radius: 8px; /* Optional: round the table corners */
  overflow: hidden; /* Prevent the rounded corners from being clipped */
}

.certifications-table th, .certifications-table td {
  padding: 10px 20px;
  text-align: left;
  font-size: 16px;
  line-height: 28px;
  font-family: "Montserrat", sans-serif;
}

.certifications-table th {
  background-color: #e9ecef; /* Light gray background for headers */
  font-weight: bold;
}

.certifications-table tr:nth-child(even) {
  background-color: #f1f3f5; /* Very light gray for even rows */
}

.certifications-table tr:nth-child(odd) {
  background-color: #ffffff; /* White for odd rows */
}

.certifications-table a {
  color: #007bff; /* Bootstrap primary blue */
  text-decoration: none;
}

/* Hover effect for table rows */
.certifications-table tr:hover {
  background-color: #f8f9fa; /* Light hover effect */
}
</style>
