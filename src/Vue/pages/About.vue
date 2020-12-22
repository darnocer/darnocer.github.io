<template>
  <section id="about" class="dark-section">
    <div class="container-fluid">
      <h1 class="section-header">{{ heading }}</h1>
      <div class="row justify-content-center">
        <div
          class="col-sm-12 col-md-6 flex-col"
          id="about-content"
          data-aos="fade-right"
          data-aos-duration="1000"
        >
          <img
            class="profile-pic float-left"
            src="../../assets/images/profile-pic.png"
            alt="profile picture"
          />

          <p id="bio">
            <span id="bio" v-html="about.bio"></span>
          </p>
        </div>
  

       <!-- <div
          class="col-sm-12 col-md-4 flex-col"
          id="facts"
          data-aos="fade-right"
          data-aos-duration="1000"
        >
          <ul class="list-group list-group-flush">
            <li v-for="item in facts" :key="item.name" class="list-group-item">
              <h3 class="d-inline">{{ item.name }}: </h3>
              <br class="d-md-none" />{{ item.value }}
            </li>
          </ul>
        </div>  -->
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
      heading: data.main.headings.about,
    };
  },
};
</script>

<style lang="scss"></style>
