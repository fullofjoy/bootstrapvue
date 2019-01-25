<template>
  <div class="content">
    <div class="input-holder">
      <input class="m-1" type="text" v-model="csvJp" placeholder="日本語"><br>
      <input class="m-1" type="text" v-model="csvEn" placeholder="英語"><br>
      <input class="m-2 btn btn-primary" type="submit" value="追加" @click="addContent">
      <h3>{{displayConcat}}</h3>
    </div>
    <hr>
    <div class="box-holder">
      <div class="box" v-for="mechanism in csv" :key="mechanism.id">
        <h4>JP:{{mechanism.japanese}}</h4>
        <p>EN:{{mechanism.english}}</p>
      </div>
    </div>
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      csv: [
        {
          japanese: 'ウェブ開発',
          english:'web developments.'
        },
        {
          japanese: 'アプリ開発',
          english:'application developments.'
        }
      ],
      csvEn:'',
      csvJp:''
    }
  },
  methods:{
    addContent() {
      if(this.csvJp && this.csvEn){
        this.csv.push({
          japanese: this.csvJp,
          english: this.csvEn
        });
        this.csvJp = '';
        this.csvEn = '';
      }else{
        return
      }
    }
  },
  computed:{
    displayConcat() {
      return this.csvJp + ' ' + this.csvEn;
    }
  }
}
</script>
 
<style scoped>
.content{
  padding: 10px;
}
.box{
  margin: 5px;
  padding: 15px;
  border: 2px solid #013892;
  float: left;
}
.box-holder:after{
  content: "";
  clear: both;
  display: table;
}
p{
  margin: 0;
}
</style>