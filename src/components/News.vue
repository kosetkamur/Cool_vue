<template>
<v-container>
    <v-row class="text-center">
      <v-col cols="12">
      <div class="wrapper">
        <div v-for="article in Articles" 
         :key="article.name" class='item'>
            <v-img
            src="images/preview.jpeg"
            height="200px"
            width="250px"
            ></v-img>
            <h2>{{ article.name}}</h2>
            <p>{{ article.date }}</p>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Articles from '../../public/articles.json';
export default {
  name: "NewsCard",

  data() {
    return {
      Articles,
    }
  },

}

</script>

<style>
.wrapper{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}
.item{
    margin: 0 30px 30px 0;
    border: 1px solid rgb(247, 247, 247);
    border-radius: 10px;
    background-color: rgb(247, 247, 247);
    padding: 20px;
    color: black;
    width: 330px;
    height: auto;
    align-content: center;
}
</style>