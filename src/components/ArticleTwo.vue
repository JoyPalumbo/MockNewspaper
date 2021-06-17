<template>
<div>
 <v-img  max-height="150"
  max-width="250"
 :src="article[9].urlToImage"></v-img>
<h5 sm8>
  {{article[9].title}}
</h5>

<!-- <h6 sm2>{{article[11].description}}</h6> -->

</div>
</template>

<script>
export default {
  name: "ArticleTwo",
  props: ["article"],
};
</script>