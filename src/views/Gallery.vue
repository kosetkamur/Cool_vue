<template>
<div class="gallery">
  <v-row>
    <v-col
        v-for="n in 9"
        :key="n"
        class="d-flex child-flex"
        cols="6"
    >
      <v-img
          src="images/full.jpeg"
          aspect-ratio="1"
          class="grey lighten-2"
      >
        <template v-slot:placeholder>
          <v-row
              class="fill-height ma-0"
              align="center"
              justify="center"
          >
            <v-progress-circular
                indeterminate
                color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
    </v-col>
  </v-row>
</div>
</template>

<script>
export default {
  name: "Gallery"
}
</script>

<style scoped>

</style>