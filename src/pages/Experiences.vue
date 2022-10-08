<template>
  <div>
    <Navbar />
    <footer class="content margin-auto">
      <article style="color: aliceblue" class="text-center">
        <section>
          <span>"{{ motto2 }}"</span>
        </section>
        <section>
          <span>--- {{ author }} ---</span>
        </section>
        <hr />
        <div v-for="e in experiences" :key="e.title">
          <section class="title">
            <span>{{ e.title }}</span>
          </section>

          <article class="skill-menu margin-auto">
            <ul class="ul-navbar">
              <li class="menu-list">
                <a href="index.html">{{ e.subtitle }}</a>
              </li>
              <li class="menu-list">
                <a href="Experiences.html">{{ e.subtitle2 }}</a>
              </li>
            </ul>
          </article>
        </div>
      </article>
    </footer>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import axios from "axios";
//https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/cartoon
export default {
  components: { Navbar },
  methods: {
    async fetchExperience() {
      try {
        let res = await axios.get(
          "https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/cartoon"
        );
        this.experiences = res.data;
      } catch (error) {}
    },
  },

  data() {
    return {
      motto2: "Life Is The Art Of Drawing Without And Eraser",
      author: "John W Gardner",
      experiences: [],
    };
  },
  beforeMount() {
    this.fetchExperience();
  },
};
</script>

<style>
</style>