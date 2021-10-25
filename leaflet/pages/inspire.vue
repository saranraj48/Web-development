<template>
  <div>
    <div id="map-wrap"></div>
    <p>hai</p>
  </div>
</template>
<script>
import l from 'nuxt-leaflet';
export default {
  mounted() {
    const map = l
      .map('map-wrap', {
        attributionControl: false,
        zoomControl: false,
      })
      .setView(l.latLng(-37.79, 175.27), 12)
    l.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
      detectRetina: true,
      maxNativeZoom: 17,
    }).addTo(map)

    const pruneCluster = new this.PruneClusterForLeaflet()
    const marker = new this.PruneCluster.Marker(59.8717, 11.1909)
    pruneCluster.RegisterMarker(marker)
    map.addLayer(pruneCluster)
  },
}
</script>
