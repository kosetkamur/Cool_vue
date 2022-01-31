<template>
  <v-container>
    <div class="wrapper">
      <h1>Добро пожаловать на наш информационный сайт!</h1>
    </div>
    <h2>Последние новости</h2>
    <NewsCard />
  </v-container>
</template>

<script>
import NewsCard from "@/components/News.vue";
export default {
name: "Main",
components: {
    NewsCard,
  },
    data () {
  },
}
</script>

<style scoped>
  .wrapper {
    padding: 200px 20px;
  }
  h1 {
    margin: 0;
    font-size: 30px;
    font-family: "Arial", sans-serif;
  }
  h2{
    padding: 20px;
  }
</style>

