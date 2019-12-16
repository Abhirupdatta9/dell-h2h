<template>
  <div>
    
    <v-img src="/hero-image.jpg" width="100vw" height="90vh">
    <v-overlay absolute>
      <v-row style="height: 200px; width: 100vw;" 
        align="end"
        justify="center">
        <p class="display-1 font-weight-light">Welcome to DELL Support</p>
      </v-row>
      <v-row style="height: 400px; width: 100vw;" 
        align="start"
        justify="center">
        <v-col sm="12" xs="12" md="5" lg="5">
          <v-text-field 
              dark  
              rounded
              
              label="How can we help you?"
              outlined
              color="blue"
              background-color="blue"
            >
            ahfafkl
            </v-text-field>
            
          </v-col>    
      </v-row>
    </v-overlay>
    </v-img>
    <br><br><br><br>
    <p class="my-12 text-center display-1 font-weight-light">Top Products</p>
    <v-row class="my-12 mx-auto" >
      <v-col cols="3" v-for="n in 4" :key="n">
        <card/>
      </v-col>
    </v-row>
     
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import card from '~/components/product-card.vue'
export default {
  components: {
    card,
  }
}
</script>

<style scoped>
.search {
  
  color: white;
}
</style>
