<template>
  <section id="about" class="dark-section">
    <div class="container-fluid">
      <h1 class="section-heading">{{ heading }}</h1>
      <div class="row justify-content-center">
      


       <div
          class="col-sm-12 col-md-6 flex-col"
          id="timeline"
          data-aos="fade-right"
          data-aos-duration="1000"
        >

        <div class="frosted" id="about-content">
          <img
            class="profile-pic float-left"
            src="../../assets/images/profile-pic.png"
            alt="profile picture"
          />

          <p id="bio">
            <span v-html="about.bio"></span>
            <!-- <a href="#" alt="Resume"><button id="resume" class="btn btn--color nav-item"><i class="far fa-file-pdf"></i> Resume</button></a> -->
          </p>
          </div>
<!-- <Timeline /> -->
         

        </div> 
      </div>
    </div>

    <Arrow />
  </section>
</template>

<script>
import data from "../../data/data.json";
import Arrow from "../components/Arrow.vue";
// import Timeline from "../components/Timeline.vue";

export default {
  name: "About",
  components: {
    Arrow,
    // Timeline
  },
  props: {},
  data() {
    return {
      about: data.about,
      name: data.main.name.first,
      facts: data.about.facts,
      heading: data.main.headings.about,
    };
  },
};
</script>

<style lang="scss"></style>
