<template>
  <div>
    <v-row>
       <v-img  
      style="margin-left : 60px"
      max-height="40"
  max-width="40"
 :src="data.data.current.condition.icon"></v-img>
 <v-col>

    <h6 style="margin-left : -40px">Weather- Temp {{data.data.current.temp_f}}<span>&#176;</span>  </h6>
    <h6 style="margin-left : -40px">{{data.data.current.condition.text}} </h6>
 </v-col>

    </v-row>
  </div>
</template>

<script>
import axios from "axios";
const url =
"http://api.weatherapi.com/v1/current.json?key=26313a917ffb443a8c5133627211606&q=Raleigh"

export default {
  name: "Weather",

  props: {},
  data() {
    return {
      data: {},
      lat: "",
      lon: "",
      city: "",
      tempC: "",
      tempF: "",
      icon: "",
      description: "cloudy",
      errorMessage: "",
    };
  },
  mounted() {
    console.log("mmmmmmmmmmeeeeeeeeeeep");
    axios
      .get(url)
      .then((data) => {
        this.data = data

        console.log("heres our data in weather", data);
        console.log(data.data.main.temp)
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>
