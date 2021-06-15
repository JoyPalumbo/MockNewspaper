<template>
  <div id="app">
    <Header />
    <h1>The Advocate</h1>
    <!-- <ul>

    <li v-for="(item) in childData" :key="item.id">{{item.title}}</li>
    <li>meep</li>
    </ul> -->
    <Newsfeed v-on:passData="getData($event)"/>
    <v-row>
 <v-col cols="2"></v-col>
    <v-col cols="8"> 

    <Carousel v-bind:images="topStories"/>
    </v-col>
    <v-col cols="2"></v-col>
    </v-row>
    <!-- <h1>{{childData[0].title}}</h1> -->
  </div>
</template>



<script>
import Header from "./components/Header";
import Newsfeed from "./components/Newsfeed";
import Carousel from "./components/Carousel"

export default {
  name: "App",
  components: {
    Header,
    Newsfeed,
    Carousel
  },
  data(){
    return{
    childData: {},
    topStories: []
    }
  },
  methods: {
    getData: function(data){
      console.log("in our get function", data)
      this.childData = data
      console.log("are we doing it right", this.childData)
      this.topStories.push(this.childData[2], this.childData[3], this.childData[4], this.childData[5])
    },
  
  }

  
};


</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  /* -webkit-font-smoothing: antialiased; */
  /* -moz-osx-font-smoothing: grayscale; */
  text-align: center;
  /* color: #2c3e50; */
  /* margin-top: 60px; */
   font-size: 1.5em;
}
</style>
