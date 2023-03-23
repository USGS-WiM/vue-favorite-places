<template>
  <!-- Layout HTML -->
  <body>
    <!-- USGS Header -->
    <div id="usgsHeader">
      <img
        src="../src/assets/images/USGS_logo.png"
        title="USGS Logo"
        alt="USGS Logo"
      />
    </div>

    <!-- Header -->
    <header id="top">
      <h1 class="app-title">App Title</h1>

      <!-- Nav -->
      <nav id="topNav" class="test">
        <a href="#">Home</a>
        <a href="#"><i class="fas fa-info-circle"></i> About</a>
        <a href="#"><i class="fas fa-arrow-right-from-bracket"></i></a>
      </nav>
    </header>

    <div id="appBody">
      <!-- Sidebar -->
      <div id="sidebar">sidebar.</div>

      <!-- Main Content Area -->
      <main id="content">
        <div id="map">
          <Map> </Map>
        </div>
      </main>
    </div>
  </body>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'*/
import "leaflet/dist/leaflet.css";
import Map from "./components/Map.vue";

export default {
  name: "App",
  components: {
    /*HelloWorld*/
    Map,
  },
};
</script>

<style>
/* Layout CSS */
body,
html {
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  min-height: 100%;
  width: 100%;
  color: var(--text);
  height: 100%;
  max-height: 100%;
  overflow: hidden;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica,
    Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
body {
  display: flex;
  flex-direction: column;
}
.test2 div {
  font-size: large;
  color: purple;
}
/* Required USGS Header */
#usgsHeader {
  display: block;
  width: 100%;
  padding: 8px 15px;
  background-color: #00264c;
  height: fit-content;
}
#usgsHeader img {
  height: 42px;
  width: auto;
}

/* Top bar */
header#top {
  width: 100%;
  background-color: black;
  display: flex;
  box-sizing: border-box;
  padding: 10px 0 10px 15px;
}
/* App title */
header#top .app-title {
  color: white;
  margin: 0;
  padding: 0;
  font-size: 18px;
  line-height: 20px;
}

/* Top Bar Navigation */
header#top nav#topNav {
  flex-grow: 3;
  display: flex;
  justify-content: flex-end;
  color: white;
  gap: 30px;
  font-size: 12px;
  margin-right: 15px;
}
/* Nav Links */
header#top nav#topNav a {
  line-height: 20px;
  color: white;
  white-space: nowrap;
}
header#top nav#topNav a i {
  padding: 0 5px;
}

/* Main Body */
div#appBody {
  flex-grow: 3;
  width: 100%;
  overflow: auto;
  max-height: 100%;
  display: flex;
  height: 100vh;
}

/* Sidebar */
#sidebar {
  background-color: yellow;
  width: 300px;
}

/* Main Content & Map */
main#content {
  background-color: seagreen;
  flex-grow: 3;
  display: flex;
  flex-direction: column;
}
/* App Content */
#mapPanel {
  display: block;
  width: 100%;
  background-color: aqua;
  min-height: 49%;
  max-height: 49%;
}
/* Map */
#map {
  width: 100%;
  height: 100%;
  background-color: orange;
}
</style>
