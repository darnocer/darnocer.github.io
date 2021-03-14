<template>
  <section id="contact" class="dark-section background-00">
    <div class="container-fluid">
      <h1 class="section-heading">{{ heading }}</h1>
      <div class="row justify-content-center">
        <!-- <div
          class="col-sm-12 col-md-6 flex-col contact-content"
          data-aos="fade-right"
          data-aos-duration="1000"
        > -->
        <!-- <div class="responsive-img">
        <img src="../../assets/images/graphics/treeswing.svg"/>
        </div> -->

        <!-- </div> -->
        <div
          class="col-sm-12 col-md-6 flex-col contact-content frosted-card"
          data-aos="fade-right"
          data-aos-duration="1000"
        >
          <h2 class="text-center">Send Me A Message</h2>


<div class="container contact-form">
  <form action="https://app.99inbound.com/api/e/q8mbJaDo" method="POST" target="_blank">
    <div class="form-group">
      <div class="input-group">
        <div class="input-group-prepend">
          <span class="input-group-text bg-white">
            <i class="fa fa-user"></i>&nbsp;
          </span>
        </div>
        <input name="name" type="name" placeholder="Name" class="form-control border-left-0" required>
      </div>
    </div>

    <div class="form-group">
      <div class="input-group">
        <div class="input-group-prepend">
          <span class="input-group-text bg-white">
            <i class="fa fa-envelope"></i>
          </span>
        </div>
        <input name="email" type="email" placeholder="Email" class="form-control border-left-0" required>
      </div>
    </div>

    <div class="form-group">
      <textarea name="message" class="form-control" id="message" rows="5" placeholder="Wazzup?" required></textarea>
    </div>

    <div style="position: absolute; left: -5000px;">
  <input type="checkbox" name="lovely_aqua_fractal_gloves" value="1" tabindex="-1" autocomplete="no">
</div>

    <button type="submit" class="btn btn--color">
      <i class="fa fa-paper-plane"></i> 
      Send
    </button>
  </form>
</div>
        </div>
      </div>
    </div>
    <div class="row arrow-container">
      <a class="arrow-icon" href="#">
        <i class="fas fa-chevron-up fa-4x"></i>
      </a>
    </div>
  </section>
</template>

<script>
import data from "../../data/data.json";

export default {
  name: "Contact",
  props: {},
  components: {},
  data() {
    return {
      contact: data.contact,
      social: data.contact.social,
      heading: data.main.headings.contact,
    };
  },
};
</script>

<style lang="scss"></style>
