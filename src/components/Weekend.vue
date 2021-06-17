<template>
  <v-card
    class="mx-auto"
    color="#778899"
    dark
    max-width="1000"
    height="300"
  >
      <h3 style="margin-bottom: 10px">

Weekend Activities
      </h3>
<v-row>
  <v-col>

        <h6>
          Interactive, multi-media art exhibit
    </h6>
    <!-- <br> -->
    <img src="../assets/advocate.jpeg" class="photos" alt="art">
  </v-col>
  <v-col>
        <h6 >
          Blues Festival and Beer Fest
    </h6>
      
    <img src="../assets/advocate2.jpeg" class="photos" alt="art">
  </v-col>
  <v-col>
        <h6>
          Kid Aecrobatics Camp
    </h6>

    <img src="../assets/advocate3.jpeg" class="photos" alt="art">
  </v-col>
</v-row>


    <v-card-actions>
      <v-list-item class="grow">

        <v-row
          align="center"
          justify="end"
        >
 

        </v-row>
      </v-list-item>
    </v-card-actions>
  </v-card>
</template>


<script>
import img1 from "@/assets/advocate.jpeg";

export default {
  name: "Weekend",
   data: function() {
    return {
      images: [img1],
    };
  },

};
</script>

<style scoped>
.h3 {
text-align: center;
 margin-bottom: 10px;

}

.photos {
  margin-top: 10px;
  padding:1px;
  width: 250px;
  height: 200px;
  border: 3px solid rgb(48, 54, 61);
  border-radius: 25px;
}
</style>