<template>
<div>
 <v-img   max-height="150"
  max-width="250"
 :src="article[8].urlToImage"></v-img>
<h5 sm6>
  {{article[8].title}}
</h5>

</div>
</template>

<script>
export default {
  name: "ArticleOne",
  props: ["article"],
    data(){
    return{

    }
  },
};
</script>