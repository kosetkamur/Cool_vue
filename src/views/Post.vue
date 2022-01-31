<template>
  <div class="wrapper">
    <h1>{{ this.post.name }}</h1>
    <v-img
          src="images/full.jpeg"
          height="200px"
          width="200px"
          class="image"
      ></v-img>

    <div class="date">{{ this.post.date }}</div>
    <p class="text">{{ this.post.desc }}</p>
    <div class="buttonBack">
    <router-link
        to="/news"
        class="back"
        height="50px"
    >Назад</router-link>
    </div>
    <div class="comment">
      <Comments v-bind:id="this.$route.params.id" />
    </div> 
  </div>
</template>

<script>
import axios from "axios";
import Comments from "../components/Comments";


export default {
  name: "Post",
  components: {Comments},
  data() {
    return {
      post: {}
    };
  },
  mounted() {
    axios
        .get(`http://demo-api.vsdev.space/api/articles/${this.$route.params.id}`)
        .then(response => (this.post = response.data));
  }
}
</script>

<style scoped>
  .wrapper {
    padding: 20px;
    display: flex;
    align-content: center;
    justify-content: center;
  }
  h1 {
    margin: 0;
    font-size: 30px;
    font-family: "Arial", sans-serif;
  }
  .back {
    display: inline-block;
    color: white;
    background-color: #a96de3;
    padding: 10px;
    width: 100px;
    box-sizing: border-box;
    text-align: center;
  }
  .text {
    font-family: "Arial", sans-serif;
    line-height: 25px;
  }
  .date {
    margin-top: 10px;
  }
  .comment{
    width: 2000px;
  }
</style>