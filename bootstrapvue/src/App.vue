<template>
  <div id="app">
    <div>
      <app-header></app-header>
      <app-content1></app-content1>
      <app-content2></app-content2>
      <app-footer></app-footer>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Content1 from "./components/Content1.vue";
import Content2 from "./components/Content2.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    'app-header': Header,
    'app-content1': Content1,
    'app-content2': Content2,
    'app-footer': Footer,
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
