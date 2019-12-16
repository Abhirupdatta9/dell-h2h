<template>
    <v-card
    class="mx-auto"
    max-width="300"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <v-card-title>Techinical service suport</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-0">Number 10</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>price</div>

      <div>inovation today tommorow</div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="orange"
        text
      >
       Explore
      </v-btn>

      
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      cards: [
        { to:"",
          title:"Waranty support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        { to:"",
          title:"Troubleshoot support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        { to:"",
          title:"Hardware support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        { to:"",
          title:"Software support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        { to:"",
          title:"Configure support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        { to:"",
          title:"Battery support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        { to:"",
          title:"Security support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        { to:"",
          title:"Premium support",
          desc: "qwdewf vfjnvlj vfknvl",
        },
        
      ]
    }
  }
}
</script>>