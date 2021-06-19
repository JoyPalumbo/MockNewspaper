<template>
<div>
 <v-img  max-height="150"
  max-width="250"
 :src="article[6].urlToImage"></v-img>
<h5 sm8>
  {{article[6].title}}
</h5>

</div>
</template>

<script>
export default {
  name: "ArticleTwo",
  props: ["article"],
};
</script>