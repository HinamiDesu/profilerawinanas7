<template>
  <div>
    <Navbar />
    <!---article-->
    <main class="content margin-auto">
      <article class="artical">
        <section class="text-center title">
          <h1>{{artical}} </h1>
        </section>

        <section class="row-50 bg-white left">
          <table class="table-cute">
            <tr>
              <td>{{ sub_article }}</td>
              <!--Emoji Windows: WIN+. or WIN+; | MAC: ^+Command+space-->
              <td>🌱🌱</td>
            </tr>
            <tr>
              <td>{{ sub_article1 }}</td>
              <td>🌱🌱🌱🌱</td>
            </tr>
            <tr>
              <td>{{ sub_article2 }}</td>
              <td>🌱🌱🌱🌱</td>
            </tr>
            <tr>
              <td>{{ sub_article3 }}</td>
              <td>🌱🌱🌱</td>
            </tr>
          </table>
        </section>
        <section class="row-50 bg-red left">
          <table class="table-cute">
            <tr>
              <td>{{ sub_article4 }}</td>
              <td>🌱🌱🌱</td>
            </tr>
            <tr>
              <td>{{ sub_article5 }}</td>
              <td>🌱🌱🌱</td>
            </tr>
            <tr>
              <td>{{ sub_article6 }}</td>
              <td>🌱🌱🌱</td>
            </tr>
            <tr>
              <td>{{ sub_article7 }}</td>
              <td>🌱🌱🌱</td>
            </tr>
          </table>
        </section>
      </article>
    </main>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import axios from "axios";
//https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/cartoon
export default {
  components: { Navbar },
  methods: {
    async fetchAbilities() {
      try {
        let res = await axios.get(
          "https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/cartoon"
        );
        this.fetchAbilities = res.data;
      } catch (error) {}
    },
  },
  data() {
    return {
      artical: "Abilities",
      sub_article: "HTML",
      sub_article1: "Canva",
      sub_article2: "English Communication",
      sub_article3: "Photography",
      sub_article4: "Drawing",
      sub_article5: "Singing",
      sub_article6: "IMovie",
      sub_article7: "Computer Graphics",
    };
  },
  beforeMount() {
    this.fetchAbilities();
  },
};
</script>

<style>
</style>