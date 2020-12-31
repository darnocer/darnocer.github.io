<template>
  <div class="banner">
    <div class="banner-text" data-aos="fade-up"
          data-aos-duration="500">
      <h2 id="greeting">Hi, I'm {{ name.first }}</h2>
      <h1 id="typewriter" class="display-text"> </h1>
    </div>
  </div>
</template>

<script>
import data from "../../data/data.json";
import Typewriter from "typewriter-effect/dist/core";

var description = data.main.description;

export default {
  name: "Banner",
  data() {
    return {
      name: data.main.name,
      // titles: data.main.titles,
      description: data.main.description,
      // greeting: data.main.greeting
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


typewriter.pauseFor(600).typeString(description).start();
    
  },
};
</script>

<style lang="scss"></style>
