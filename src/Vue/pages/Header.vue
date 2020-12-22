<template>
  <header id="home" class="bg">
    <nav class="navbar navbar-expand-lg fixed-top dark-bg">
             <div v-if="logo"><img src="../../assets/images/logo.png" alt="logo" id="Logo"></div>
        <div v-if="!logo">
          <span id="FirstName">{{main.name.first}}</span> <span id="LastName">{{main.name.last}}</span>
        </div>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"><i class="fas fa-bars" style="color:#fff; font-size:28px;"></i></span>
      </button>
      <div id="navbarNavAltMarkup" class="collapse navbar-collapse">
        <ul id="navbar-nav" class="navbar-nav ml-auto">
          <li class="active-nav">
            <a class="nav-item nav-link" href="#home">Home</a>
          </li>
          <li><a class="nav-item nav-link" href="#about">About</a></li>
          <li><a class="nav-item nav-link" href="#skills">Skills</a></li>
          <li><a class="nav-item nav-link" href="#portfolio">Portfolio</a></li>
          <li><a class="nav-item nav-link" href="#contact">Contact</a></li>
          
        </ul>
        <ul class="navbar-nav">
          <li><a href="https://blog.darnocer.io" target="_blank" alt="Darian's Blog"><button class="nav-item nav-link btn btn--color" id="btn--blog">Blog <i class="fas fa-external-link-alt"></i></button></a></li></ul>
      </div>
    </nav>
    <Banner />
    <div class="row arrow-container" data-aos="fade-up" data-aos-duration="3000" data-aos-delay="3000">
    <a href="#about" class="arrow-icon" role="button">
      <i class="fas fa-chevron-down fa-4x"></i>
    </a>
  </div>
  </header>
</template>

<script>
// import Arrow from "../components/Arrow.vue";
import data from "../../data/data.json";
import Banner from "../components/Banner.vue";

export default {
  name: "Header",
  components: {
    Banner,
    // Arrow,
  },
  props: {},
  data() {
    return {
      name: data.main.name,
      logo: data.main.logo
    };
  },
};
</script>

<style lang="scss"></style>
