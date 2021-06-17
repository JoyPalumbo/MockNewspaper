<template>
  <div>
    <v-row>
      <!-- <v-col cols="8"></v-col> -->
<!-- <v-col> -->
       <v-img  
      style="margin-left : 60px"
      max-height="40"
  max-width="40"
 :src="data.data.current.condition.icon"></v-img>
<!-- </v-col> -->
 <v-col>

    <h6 style="margin-left : -40px">Weather- Temp {{data.data.current.temp_f}}<span>&#176;</span>  </h6>
    <h6 style="margin-left : -40px">{{data.data.current.condition.text}} </h6>
 </v-col>
<!-- </v-col>  -->
  
<!-- <v-col cols="1"> -->

    </v-row>
  </div>
</template>

<script>
import axios from "axios";
const url =
"http://api.weatherapi.com/v1/current.json?key=26313a917ffb443a8c5133627211606&q=Raleigh"
  // "http://api.weatherapi.com/v1/current.json?key=26313a917ffb443a8c5133627211606&q=London";
// "api.openweathermap.org/data/2.5/weather?q=London&appid=301a5f02ab435c9dcd29263f8ae55d3c"
// "http://api.openweathermap.org/data/2.5/weather?q=London&appid=301a5f02ab435c9dcd29263f8ae55d3c"

// https://dataservice.accuweather.com/currentconditions/v1/5h7HEGYGZ9VGq5t2PbjyaWMJPrucT2N6

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

  // methods: {
  // getLocation() {
  //   if (navigator.geolocation) {
  //   console.log("we have a location")
  //    navigator.geolocation.getCurrentPosition(showPosition);
  //   } else {
  //     alert("Geolocation is not supported by this browser. Please add a city.");
  // 		enterLocation();
  //     console.log("no location")
  //   }
  // },

  // getWeather() {
  //   axios.get('http://api.weatherapi.com/v1')
  // }
  // },
};
</script>
