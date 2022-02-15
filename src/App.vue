<template>
  <ArcGISMap msg="ArcGIS Map Template"/>
</template>

<script>
  import ArcGISMap from './components/ArcGISMap.vue'

  export default {
    name: 'App',
    components: {
      ArcGISMap
    }
  }
</script>

<style>
  @import url('https://js.arcgis.com/4.22/esri/themes/dark/main.css');
  html, body {
    width: 100%;
    height: 100%;
    padding: 0;
    margin: 0;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    height: 100%;
    width: 100%;
  }
</style>
