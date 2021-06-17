<template>
  <v-footer
    dark color="#162130"
    padless
    sm2
  >
  <v-container>

  
    <v-row
      justify="center"
      no-gutters
    >

    <v-col cols="3">

    <div class="underline" style="margin-bottom: 10px">Sections</div>

      <div class="footerText">Home</div>
        <div class="footerText">About Us</div>
      <div class="footerText">Sports</div>
        <div class="footerText">Entertainment</div>
          <div class="footerText">Calendar</div>
  
      <!-- <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        font-size="17px"
        class="my-2"
        
      >
        {{ link }}
      </v-btn> -->
    <!-- </div> -->
        <v-col cols="1"></v-col>
    </v-col>
    <v-col cols="3">
      <div class="underline" style="margin-bottom: 10px">Services</div>
        <div class="footerText">Subscribe</div>
      <div class="footerText">Classifieds</div>
        <div class="footerText">Ad Space</div>
          <div class="footerText">Community</div>
            <div class="footerText">Calendar</div>
    </v-col>

        <v-col cols="3">
   <div class="underline" style="margin-bottom: 10px">Contact Us</div>

   <div class="footerText">The Advocate</div>
   <div class="footerText">123 Main St</div>
   <div class="footerText">Town, NC 12345</div>
   <div class="footerText">Phone: 555-123-1234</div>
   <div class="footerText">Email: info@advocate.com</div>
 </v-col>
 <v-col cols="3">
   
   <div class="underline" style="margin-bottom: 10px">Follow Us</div>
   <v-row>
     <v-col cols="3"></v-col>
<v-col cols="2">

   <i class="fa fa-facebook-square" aria-hidden="true"></i>
</v-col>
<v-col cols="2">

   <i class="fa fa-twitter-square" aria-hidden="true"></i>
</v-col>
<v-col cols="2">

   <i class="fa fa-instagram" aria-hidden="true"></i>
</v-col>
   </v-row>
         
    </v-col>

      </v-row>
      <v-row       

      no-gutters>

      <v-col
        class="primary lighten-2 text-center white--text sm2"
        cols="12"
      >
      <div class="footerText">

        {{ new Date().getFullYear() }} — The Advocate
      </div>
      </v-col>
    </v-row>

    </v-container>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
    }),
  }
</script>

<style>
.underline {
  /* text-decoration: underline; */
  font-size: 17px;
   -webkit-text-decoration: slateblue solid underline;
  text-decoration: slateblue solid underline;
  -webkit-text-underline-position: under;
  text-underline-position: under;
    /* -webkit-text-decoration: darkturquoise solid underline;
  text-decoration: darkturquoise solid underline;
  -webkit-text-decoration-skip: ink;
  text-decoration-skip: ink; */
}
.footerText {
  font-size: 14px;
  /* margin: 1px; */
}


</style>