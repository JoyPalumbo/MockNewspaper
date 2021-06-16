<template>
<div>
 <v-img   max-height="150"
  max-width="250"
 :src="article[8].urlToImage"></v-img>
<h5 sm6>
  {{article[8].title}}
</h5>
<!-- <v-img

  max-height="150"
  max-width="250"
  :src="article.urlToImage"
></v-img> -->

 <!-- <v-img :src="article[10].urlToImage"></v-img> -->
<!-- <h6 sm1 >{{article[10].description}}</h6> -->


</div>
</template>

<script>
export default {
  name: "ArticleOne",
  props: ["article"],
    data(){
    return{
      // description: this.article[10].description
    }
  },
};
</script>