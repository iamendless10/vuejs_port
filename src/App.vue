<template>
  <div>
    <NavBar/>
    <LandingPage/>
    <SplitPage/>
    <CodingPage/>
    <ProfilesContainer/>
    <RecognitionsContainer/>
    <MyselfPage/>
    <WorkExperience/>
  
    <TechnicalStackComponent/>
    <HeadingComponent/>
    <ProjectsComponent/>
    <CertificationsComponent/>
    <AchievementsHeading/>
    <AchievementsContainer/>
    <GalleryOfAccomplishments/>
    <ContactUs/>
  
    
  </div>
  

</template>

<script>
import NavBar from './components/NavBar.vue';
import SplitPage from './components/SplitPage.vue';
import CodingPage from './components/CodingPage.vue';
import ProfilesContainer from './components/ProfilesContainer.vue';
import RecognitionsContainer from './components/RecognitionsContainer.vue';
import MyselfPage from './components/MyselfPage.vue';
import WorkExperience from './components/WorkExperience.vue';

import TechnicalStackComponent from './components/TechnicalStackComponent.vue';
import ProjectsComponent from './components/ProjectsComponent.vue';
import HeadingComponent from './components/HeadingComponent.vue';
import CertificationsComponent from './components/CertificationsComponent.vue';
import AchievementsContainer from './components/AchievementsContainer.vue';
import AchievementsHeading from './components/AchievementsHeading.vue';
import GalleryOfAccomplishments from './components/GalleryOfAccomplishments.vue';
import ContactUs from './components/ContactUs.vue';
import LandingPage from './components/LandingPage.vue';


export default {
  name: 'App',
  components: {
    NavBar,
    SplitPage,
    CodingPage,
    ProfilesContainer,
    RecognitionsContainer,
    MyselfPage,
    WorkExperience,
  
    TechnicalStackComponent,
    ProjectsComponent,
    HeadingComponent,
    CertificationsComponent,
    AchievementsContainer,
    AchievementsHeading,
    GalleryOfAccomplishments,
    ContactUs,
    LandingPage
  
  }
}
</script>

<style>
#app {
 
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

html{
  scroll-behavior: smooth;
}
</style>
