<template>
  <div id="map-wrap" style="height: 100vh">
    <client-only>
      <l-map :zoom="13" :center="[11.892078, 79.827851]">
        <l-tile-layer
          url="http://{s}.tile.osm.org/{z}/{x}/{y}.png"
        ></l-tile-layer>
      </l-map>
    </client-only>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { loc: [11.892078, 79.827851], title: 'pondy' },
        { loc: [13.892078, 18.827851], title: 'chennai' },
      ],
    }
  },
}
</script>
