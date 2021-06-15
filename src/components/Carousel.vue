<template>
<!-- <v-flex xs12> -->


  <v-carousel hide-delimiters cycle height="300" width="200"  :show-arrows="false">
    <v-carousel-item
      v-for="(image,i) in images"
      :key="i"
      :src="image.urlToImage"
    > 
     <div class="title">{{image.title}}</div>
      <!-- <v-sheet
        tile
      > -->
        <!-- <v-row
          class="d-flex align-end mb-6"

        > -->
          <!-- <div class="text-h2">
            {{image.title}}
          </div> -->
        <!-- </v-row> -->
      <!-- </v-sheet> -->
          </v-carousel-item>


  </v-carousel>
<!-- </v-flex> -->
</template>

<script>
export default {
  name: "Carousel",
  props: ["name", "images"],
  data () {
      return {
       
      }

  }
};
</script>

<style scoped>
.title {
  color: white;
  position: absolute;
  bottom: 0px;
  right: 50px;
  left: 50px;
  justify-content: center;
  /* align-content: center; */
  background-color: rgba(0,0,0,0.5);
  /* padding: 5px; */
  /* z-index: 2; */
  
}
</style>