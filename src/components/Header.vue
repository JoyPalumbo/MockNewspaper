<template>
  <v-app-bar>
    <v-toolbar dark color="#162130" height="35vh" fixed>
      <v-toolbar-title class="white--text">
      </v-toolbar-title>
      <v-toolbar-items >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
      </v-btn>

                <!-- <v-text-field
          solo
          placeholder="Search"
          single-line
          append-icon="search"
          background-color="#202d3f"
          color="white"
          hide-details
  
        ></v-text-field> -->
      </v-toolbar-items>

      <v-spacer></v-spacer>

      <v-layout row align-center style="max-width: 30vw; min-width: 1vw;  ">
        <v-text-field

          placeholder="Search"
          single-line
          append-icon="search"
          background-color="#202d3f"
          color="white"
          hide-details
       
        ></v-text-field>
      </v-layout>
    </v-toolbar>
    <!-- <div>
      <h1>The Advocate</h1>
    </div> -->
  </v-app-bar>
</template>

<script>
export default {
  name: "Header",
  props: {

  },
      data: () => ({
      links: [
        'Home',
        'About Us',
        'Entertainment',
        'Sports',
        'Community',
      ],
    }),
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
} */
</style>
  