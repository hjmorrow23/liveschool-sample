<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body {
  margin: 0;
}

@font-face {
  font-family: 'Lato';
  src: url('~@/assets/fonts/Lato/Lato-Regular.ttf');
  font-weight: normal;
  font-style: normal;
}

#app {
  font-family: 'Lato', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: relative;
  /* margin-top: 60px; */
  height: 100vh;
  overflow: hidden;
  width: 100%;
}

</style>
