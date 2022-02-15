<template>
  <div class='map-arcgis'></div>
</template>

<script>
import Map from '@arcgis/core/Map';
import MapView from '@arcgis/core/SceneView';

import esriConfig from '@arcgis/core/config.js';

export default {
  name: 'ArcgisMap',
  props: {
    msg: String
  },
  mounted() {
    esriConfig.assetsPath = './assets';

    let date = new Date();

    const map = new Map({
      map, 
      container: this.$el,
      zoom: 16,
      camera: {
        position: [-93.616, 41.589, 32000],
        heading: 0
      },
      environment: {
        starsEnabled: true,
        atmosphereEnabled: true,
        lighting: {
          date: date,
          directShadowsEnabled: true
        }
      }
    });

    view.when(() => {
      console.log('view ready');
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.map-arcgis{
  height: 100%;
  width: 100%;
}
</style>
