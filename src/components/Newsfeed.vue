<template>
<div ></div>
</template>

<script>
import axios from "axios";
// const API_KEY = "88d4578072c548ad8a2b1017058273c4";
const url =
  "https://newsapi.org/v2/top-headlines?country=us&apiKey=88d4578072c548ad8a2b1017058273c4";
// axios.get(url).then((data) => {
//   console.log(data);
// });

export default {
  name: "Newsfeed",
 
  mounted(){
axios.get(url).then((data) => {
  console.log(data.data.articles);
  this.data = data.data.articles
  console.log("checking data", data)
 this.passData()
});
  },
  data(){
    return {
      data: this.data
    }
  },
  methods: {
    passData: function(){
      this.$emit('passData', this.data)
    }
  }
}



</script>