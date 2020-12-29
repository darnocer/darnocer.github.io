<template>
  <section id="about" class="dark-section">
    <div class="container-fluid">
      <h1 class="section-header">{{ heading }}</h1>
      <div class="row">
        <div
          class="col-sm-12 col-md-6 flex-col"
          data-aos="fade-right"
          data-aos-duration="1000"
        >
        <div id="about-content">
          <img
            class="profile-pic float-left"
            src="../../assets/images/profile-pic.png"
            alt="profile picture"
          />

          <p id="bio">
            <span v-html="about.bio"></span>
          </p>
          </div>
        </div>
  

       <div
          class="col-sm-12 col-md-6 flex-col"
          id="timeline"
          data-aos="fade-right"
          data-aos-duration="1000"
        >
          <div class="timeline">
            <div v-for="item in timeline" :key="item.name" class="timeline-item frosted">
              <div class="timeline-content">
              <h3 class="year">{{item.year}}</h3>
              <h2>{{item.title}}</h2>
              <p>{{item.description}}</p>
              </div>
            </div>

          </div>

        </div> 
      </div>
    </div>

    <Arrow />
  </section>
</template>

<script>
import data from "../../data/data.json";
import Arrow from "../components/Arrow.vue";

export default {
  name: "About",
  components: {
    Arrow,
  },
  props: {},
  data() {
    return {
      about: data.about,
      name: data.main.name.first,
      facts: data.about.facts,
      timeline: data.about.timeline,
      heading: data.main.headings.about,
    };
  },
};
</script>

<style lang="scss"></style>
