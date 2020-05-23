<template>
  <v-app class="myFont">
    <navbar/>
    <v-content>
      <home/>
    </v-content>
  </v-app>
</template>

<script>
import home from '../src/components/Home'
import navbar from '../src/components/Navbar'

export default {
  name: 'App',
  components: {
    home, navbar
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
  font-size: 12px;
}
</style>
