<template>
  <header id="home" class="bg">
    <nav class="navbar navbar-expand-lg fixed-top dark-bg">
      <a class="navbar-brand" href="#" style="text-transform:lowercase;"
        ><span id="FirstName" >{{name.first}}</span><span id="LastName">{{name.last}}.</span></a
      >
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
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
      </div>
    </nav>
    <Banner />
    <div class="row arrow-container" data-aos="fade-up" data-aos-duration="1000">
    <a href="#about" class="arrow-icon" role="button">
      <p>Tell me more</p>
      <i class="fas fa-chevron-down fa-4x"></i>
    </a>
  </div>
  </header>
</template>

<script>
// import Arrow from "../components/Arrow.vue";
import data from "../data/data.json";
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
    };
  },
};
</script>

<style lang="scss"></style>
