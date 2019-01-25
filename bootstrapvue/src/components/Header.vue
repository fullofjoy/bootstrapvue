<template>
  <header>
    <h1>{{title}}</h1>
    <p>{{subTitle}}</p>
  </header>
</template>

<script>
export default {
  data() {
    return{
      title: "Leafhub.",
      subTitle: "powered by vue.js"
    }
  }
}
</script>

<style>
header{
  background-color:white;
  text-align: center;
  padding: 10px;
}
h1{
  color: blue;
  margin: 0;
}
p{
  color: #999;
  margin: 0;
}
</style>