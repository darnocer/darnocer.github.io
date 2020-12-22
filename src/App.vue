<template>
  <div id="app">
    <Header />
    <About />
    <!-- <Skills /> -->
    <Projects />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Header from "./Vue/pages/Header.vue";
import About from "./Vue/pages/About.vue";
// import Skills from "./Vue/pages/Skills.vue";
import Projects from "./Vue/pages/Projects";
import Contact from "./Vue/pages/Contact.vue";
import Footer from "./Vue/pages/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    About,
    // Skills,
    Projects,
    Contact,
    Footer,
  },
};
</script>

<style>
@import "./styles/css/main.css";
</style>
