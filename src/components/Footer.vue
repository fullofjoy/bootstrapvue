<template>
  <footer>
    <p>{{addr}}</p>
    <p>{{copyright}}</p>
  </footer>
</template>

<script>
export default {
  data() {
    return{
      addr: "〒123-4567 千葉県千葉市中央区 1-1-1",
      copyright: "leafhub. All right reserve."
    }
  }
}
</script>

<style>
footer{
  background-color: #c9c9c9;
  text-align: center;
}
h1{
  color: #012344;
  margin: 0;
}
p{
  color: #000;
  margin: 0;
}
</style>
