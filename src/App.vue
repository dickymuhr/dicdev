<template>
  <Home/>
</template>

<script>
import Home from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
#app {
  width: 100%;
  height: 100%;
  font-family: 'StudioFeixenSans', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background-color: #04192C; /* This will set the background color for the full page */
  font-family: 'StudioFeixenSans', Arial, sans-serif;
}

@font-face {
  font-family: 'StudioFeixenSans';
  src: url('@/assets/fonts/StudioFeixenSansTRIAL-Light.woff') format('woff');
  font-weight: 300; /* Light */
  font-style: normal;
}

@font-face {
  font-family: 'StudioFeixenSans';
  src: url('@/assets/fonts/StudioFeixenSansTRIAL-Regular.woff') format('woff');
  font-weight: 400; /* Regular */
  font-style: normal;
}

@font-face {
  font-family: 'StudioFeixenSans';
  src: url('@/assets/fonts/StudioFeixenSansTRIAL-Medium.woff') format('woff');
  font-weight: 500; /* Medium */
  font-style: normal;
}

@font-face {
  font-family: 'StudioFeixenSans';
  src: url('@/assets/fonts/StudioFeixenSansTRIAL-Semibold.woff') format('woff');
  font-weight: 600; /* Semibold */
  font-style: normal;
}

@font-face {
  font-family: 'StudioFeixenSans';
  src: url('@/assets/fonts/StudioFeixenSansTRIAL-Bold.woff') format('woff');
  font-weight: 700; /* Bold */
  font-style: normal;
}
</style>
