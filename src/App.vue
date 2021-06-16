<template>
  <v-container id="app">
    <Header />
    <v-row>
       <v-col md="3">
        
       </v-col>
 <v-col md="6">
 
    <h1>The Advocate</h1>
 </v-col>
  <v-col md="3"></v-col>
    </v-row>
    <v-row>
            <v-col md="3">
        
       </v-col>
 <v-col md="6">
 
    <h6>06/15/2021</h6>
 </v-col>
  <v-col md="3"></v-col>
    </v-row>
    <!-- <v-divider class="hr"></v-divider>
    <v-spacer class="ma-1"></v-spacer>
 <v-divider class="hr2"></v-divider> -->
<!-- <v-spacer class="ma-1"></v-spacer> -->


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
    <v-spacer class="ma-1"></v-spacer>
    <v-spacer class="ma-1"></v-spacer>
    <br>
    <br>
    <!-- <v-divider class="hr2"></v-divider> -->
    
    <v-row> 
       
      <!-- <v-divider vertical></v-divider> -->
           
      <v-col cols="4">
        <ArticleOne v-bind:article="childData"/>
      </v-col>
    <!-- <v-divider vertical></v-divider> -->
    <v-col cols="4">

    <ArticleTwo v-bind:article="childData"/>
</v-col>
<!-- <v-divider vertical></v-divider> -->
    <v-col cols="4">

    <ArticleThree v-bind:article="childData"/>
</v-col>
<!-- <v-divider vertical></v-divider> -->
    </v-row>  
          <v-spacer class="ma-1"></v-spacer>
    <v-spacer class="ma-1"></v-spacer>
   
        
<br>
<br>
  <Footer />
  </v-container>
</template>



<script>
import Header from "./components/Header";
import Footer from "./components/Footer";
import Newsfeed from "./components/Newsfeed";
import Carousel from "./components/Carousel";
import ArticleOne from "./components/ArticleOne";
import ArticleTwo from "./components/ArticleTwo";
import ArticleThree from "./components/ArticleThree";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Newsfeed,
    Carousel,
    ArticleOne,
    ArticleTwo,
    ArticleThree
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
  /* font-family: "Avenir", Helvetica, Arial, sans-serif; */
  /* -webkit-font-smoothing: antialiased; */
  /* -moz-osx-font-smoothing: grayscale; */
  text-align: center;
  /* color: #2c3e50; */
  /* margin-top: 60px; */
   font-size: 1.5em;
}
hr {
    border: none;
    height: 1px;
    /* Set the hr color */
    color: #333; /* old IE */
    background-color: #333; /* Modern Browsers */
}
hr2 {
    border: none;
    height: 1px;
    /* Set the hr color */
    color: #333; /* old IE */
    background-color: #333; /* Modern Browsers */
}
</style>
