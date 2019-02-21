<template>
  <div id="app">
    <Header/>
    <router-view/>
  </div>
</template>
<script>

import Header from "./components/layout/Header";

export default {
  name: 'app',
  components: {
    Header
  }
}
</script>

<style>
* {
  margin: 0px;
  padding: 0px;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.btn {
  background: #555;
  color: #fff;
  border: none;
}
</style>
