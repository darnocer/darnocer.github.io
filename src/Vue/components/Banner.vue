<template>
  <div class="banner">
    <div class="banner-text" data-aos="fade-up"
          data-aos-duration="500">
      <h3 class="greeting-subtitle">Hi, I'm {{ name.first }}</h3>
      <h1 id="typewriter" class="display-text"> </h1>
      <!-- <h2 id="typewriter"></h2> -->
    </div>
  </div>
</template>

<script>
import data from "../../data/data.json";
import Typewriter from "typewriter-effect/dist/core";

var titles = data.main.titles;
// var description = data.main.description;

export default {
  name: "Banner",
  data() {
    return {
      name: data.main.name,
      titles: data.main.titles,
      description: data.main.description,
      greeting: data.main.greeting
    };
  },
  mounted: function() {
   var typewriter = new Typewriter("#typewriter", {
      // strings: titles,
      // strings: description,
      delay: 100,
      autoStart: true,
      loop: false,
      deleteSpeed: 5,
    });

typewriter.pauseFor(600).typeString(titles[0]).pauseFor(100).deleteAll(5).typeString(titles[1]).pauseFor(100).deleteAll(5).typeString(titles[2]).start()
    
  },
};
</script>

<style lang="scss"></style>
