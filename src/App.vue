<template>
  <v-app class="myFont">
    <v-app-bar
      app
      color="primary"
      dark
    >
    </v-app-bar>

    <v-content>
      <home/>
    </v-content>
  </v-app>
</template>

<script>
import home from '../src/components/home'

export default {
  name: 'App',
  components: {
    home
  },
  data() {
    return {
      
    }
  },
  methods:{
    
  },
};
</script>

<style>
.myFont{
  font-family: "VSCO Gothic", -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol" !important
}
</style>
