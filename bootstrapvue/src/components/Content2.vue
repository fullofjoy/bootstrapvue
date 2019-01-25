<template>
  <div class="content mb-4">
    <hr>
    <ul class="list-group">
      <li class="list-group-item" v-for="(item, i) in list" :key="item">{{ item }}
        <button class="btn btn-danger" @click="list.splice(i, 1)">削除</button>
      </li>
    </ul>
    <button class="btn btn-primary text-center" @click="addItem">追加</button>
    <p>Length: {{ length }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
      list: ['リンゴ', 'バナナ', 'イチゴ']
    }
  },
  computed: {
    length: function() {
      return this.list.length
    }
  },
  methods: {
    addItem: function() {
      this.list.push('ミカン' + (++this.counter).toString())
    }
  }
}
</script>

<style>
  ul {
    border: 2px;
  }
</style>