<template>
  <v-app class="myFont">
    <navbar/>
    <v-content>
      <router-view></router-view>
    </v-content>
    <v-footer/>
  </v-app>
</template>

<script>
import navbar from '../src/components/Navbar'
import footer from '../src/components/Footer'

export default {
  name: 'App',
  components: {
    navbar, 'v-footer': footer
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
  font-family: "VSCO Gothic", -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol" !important;
}
</style>
