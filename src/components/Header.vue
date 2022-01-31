<template>
  <v-container>
    <v-toolbar
        color="grey"
        flat
    >
      <v-toolbar-items>
        <v-btn
            text
            color="#FFFFFF"
        >
          <router-link
              to="/"
              color="#FFFFFF"
          >НОВОСТИ МИРА</router-link>
        </v-btn>
        <v-btn
            text
            color="#FFFFFF"
        >
          <router-link
              to="/"
              color="#FFFFFF"
          >Главная</router-link>
        </v-btn>
        <v-btn
            text
            color="#FFFFFF"
        >
          <router-link to="/news">Новости</router-link>
        </v-btn>
        <v-btn
            text
            color="#FFFFFF"
        >
          <router-link to="/about">О нас</router-link>
        </v-btn>
        <v-btn
            text
            color="#FFFFFF"
        >
          <router-link to="/gallery">Галерея</router-link>
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <v-text-field
          v-model="search"
          class="search mt-6"
          placeholder="Поиск"
          prepend-inner-icon="mdi-magnify"
          filled
          dense
      ></v-text-field>
    </v-toolbar>
  </v-container>
</template>

<script>
export default {
name: "Header",
  data: () => ({
    search: null,
}),
}
</script>

<style scoped>
.v-application a {
  color: white;
  text-decoration: none;
}

.v-input.search .v-input__slot .v-input__slot:before, .v-input.search .v-input__slot .v-input__slot:before {
  border: 1px solid grey;
}
.v-input.search.closed{
  max-width: 45px;
}

.v-input.search.closed.v-input__slot {
  background: transparent !important;
}

</style>