<template>
  <v-app id="sandbox">
    <!-- <v-navigation-drawer
      
      v-model="primaryDrawer.model"
      :clipped="primaryDrawer.clipped"
      :floating="primaryDrawer.floating"
      :mini-variant="primaryDrawer.mini"
      :permanent="primaryDrawer.type === 'permanent'"
      :temporary="primaryDrawer.type === 'temporary'"
      app
      overflow
    /> -->

    <v-app-bar
      color="blue"
      class="white--text"
      :clipped-left="primaryDrawer.clipped"
      app
    >
      <!-- <v-app-bar-nav-icon
      dark
        
        v-if="primaryDrawer.type !== 'permanent'"
        @click.stop="primaryDrawer.model = !primaryDrawer.model"
      /> -->
      <v-toolbar-title>DELL TECHNOLOGIES</v-toolbar-title>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      <v-btn text class="white--text" to="/">Home</v-btn>
      <v-btn text to="/services-support" class="white--text">Services</v-btn>
      <v-btn text class="white--text">About Us</v-btn>
      <v-btn text class="white--text">Contact</v-btn>
      <v-btn text class="white--text">Help</v-btn>
    </v-app-bar>

    
   
      <nuxt/>
   
    <!-- <v-footer
      :inset="footer.inset"
      app
    >
      <span class="px-4">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer> -->
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawers: ['Default (no property)', 'Permanent', 'Temporary'],
      primaryDrawer: {
        model: null,
        type: 'default (no property)',
        clipped: false,
        floating: false,
        mini: false,
      },
      footer: {
        inset: true,
      },
    }),
  }
</script>