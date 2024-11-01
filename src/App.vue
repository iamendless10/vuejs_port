<template>
  <div id="app">
    <NavBar />
    <LandingPage />
    <transition name="fade">
      <SplitPage />
    </transition>
    <transition name="fade">
      <HeadingComponent />
    </transition>
    <transition name="fade">
      <ProjectsComponent />
    </transition>
    <transition name="fade">
      <RecognitionsContainer />
    </transition>
    <transition name="fade">
      <MyselfPage />
    </transition>
    <!-- <transition name="fade">
      <CodingPage />
    </transition> -->
    <!-- <transition name="fade">
      <ProfilesContainer />
    </transition> -->
    <transition name="fade">
      <WorkExperience />
    </transition>
    <transition name="fade">
      <TechnicalStackComponent />
    </transition>
    <transition name="fade">
      <CertificationsComponent />
    </transition>
    <transition name="fade">
      <AchievementsHeading />
    </transition>
    <transition name="fade">
      <AchievementsContainer />
    </transition>
    <transition name="fade">
      <GalleryOfAccomplishments />
    </transition>
    <transition name="fade">
      <ContactUs />
    </transition>
    <transition name="fade">
      <FooterComponent />
    </transition>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import SplitPage from './components/SplitPage.vue';
// import CodingPage from './components/CodingPage.vue';
// import ProfilesContainer from './components/ProfilesContainer.vue';
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
import FooterComponent from './components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    SplitPage,
    // CodingPage,
    // ProfilesContainer,
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
    LandingPage,
    FooterComponent,
  },
};
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

html {
  scroll-behavior: smooth;
}

/* Transition styles */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
}
</style>
