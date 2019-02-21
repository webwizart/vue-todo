<template>
  <header class="header">
    <h1>
      <img src="https://vuejs.org/images/logo.png" alt="vue.js logo">
      TodoList
    </h1>

    <nav id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.header {
  background-color: black;
  color: #fff;
  margin-top: 0;
  text-align: center;
  padding: 1%;
}
.header a {
  color: #fff;
  padding: 5px;
  text-decoration: none;
}
header img {
  width: 25px;
}
</style>
