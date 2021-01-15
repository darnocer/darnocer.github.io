<template>
  <footer class="footer section-dark font-small text-center">
    <ul class="list-inline">
      <li class="list-inline-item">
        <a class="nav-item nav-link active hover-effect" href="#">
          Home
        </a>
      </li>
      <li class="list-inline-item">
        <a class="nav-item nav-link hover-effect" :href="'mailto:'+ email" :title="email">Email</a>
      </li>
      <!-- <li class="list-inline-item">
        <a class="nav-item nav-link" href="#skills">Skills</a>
      </li> -->
      <li class="list-inline-item">
        <a class="nav-item nav-link hover-effect" :href="resume" target="_blank">Resume</a>
      </li>
      <li class="list-inline-item">
        <a class="nav-item nav-link hover-effect" :href="blog" target="_blank">Blog</a>
      </li>
      <li class="list-inline-item">
        <a class="nav-item nav-link hover-effect" href="https://www.theunderdogfoundation.org" target="_blank">#TUF</a>
      </li>
    </ul>

    <ul class="list-inline">
      <li
        v-for="(item, i) in social"
        :key="i"
        class="social-item list-inline-item"
      >
        <a :href="item.url" target="_blank" :alt="item.name" class="social-icon">
          <i :class="item.faClass"> </i>
        </a>
      </li>
    </ul>

    <div class="copyright">
      <p>
        Copyright © {{ new Date().getFullYear() }} {{ text.main.name.first }}
        {{ text.main.name.last }}.
        {{ text.footer.copyrightText }}
      </p>
    </div>
    <div class="credit">
      <p>
        Designed with 👽 by
        <a
        class="hover-effect"
          id="username"
          href="https://www.github.com/darnocer"
          alt="Darian's Github"
          >darnocer</a
        >
      </p>
    </div>
  </footer>
</template>

<script>
import data from "../../data/data.json";

export default {
  name: "Footer",
  components: {},
  props: {},
  data() {
    return {
      text: data,
      social: data.contact.social,
      resume: data.contact.resumeLink,
      email: data.contact.email,
      blog: data.contact.blog,
      location: data.contact.location
    };
  },
};
</script>

<style lang="scss"></style>
