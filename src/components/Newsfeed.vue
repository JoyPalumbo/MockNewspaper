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
  // data: {

  // }
}
// mounted(){ 
// axios.get(url).then((data) => {
//   console.log(data);
// });
// }

// data: {

// }
// const RSS_URL = `https://news.google.com/news/rss`;

// fetch(RSS_URL)
//   .then(response => response.text())
//   .then(str => new window.DOMParser().parseFromString(str, "text/xml"))
//   .then(data =>
//   console.log(data))
//       console.log(data);
//     const items = data.querySelectorAll("item");
//     let html = ``;
//     items.forEach(el => {
//       html += `
//         <article>
//           <img src="${el.querySelector("link").innerHTML}/image/large.png" alt="">
//           <h2>
//             <a href="${el.querySelector("link").innerHTML}" target="_blank" rel="noopener">
//               ${el.querySelector("title").innerHTML}
//             </a>
//           </h2>
//         </article>
//       `;
//     });
//     document.body.insertAdjacentHTML("beforeend", html);
</script>