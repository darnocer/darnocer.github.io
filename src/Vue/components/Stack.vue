<template>
  
 <div class="tool-stack"  data-aos="fade-right"
          data-aos-duration="1000">
    <div class="row flex-row align-items-center justify-content-center">
      <h3 class="tools-label">My Tools:</h3>
      <div class="tool-item" v-for="skill in skills" :key="skill.name">
        <a href="#projects" :title="skill.name"><img class="tool-logo" :src="require(`../../assets/images/portfolio/skills/${skill.image}.png`)" /></a>
        </div>
      </div>
      </div>

 
</template>

<script>

import data from "../../data/data.json";

export default {
  name: "Stack",
  props: {},

 data() {
    return {
    timeline: data.about.timeline,
    skills: data.portfolio.skills
    }
}
}

</script>

<style lang="scss"></style>
