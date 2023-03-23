
<template>
  <div id="map"></div>
</template>

<script>
import "leaflet/dist/leaflet.css";
import L from "leaflet";

export default {
  name: "Map",
  data() {
    return {
      center: [37.7749, -122.4194],
    };
  },
  methods: {
    setupLeafletMap: function () {
      const mapDiv = L.map("map").setView(this.center, 13);
      L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
        attribution:
          'Map data (c) <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery (c) <a href="https://www.mapbox.com/">Mapbox</a>',
        maxZoom: 18,
      }).addTo(mapDiv);
      this.map.addControl(L.Control.Layers);
    },
  },
  mounted() {
    this.setupLeafletMap();
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
