<template>
  <div>
    <h1>こんにちは</h1>
    <div>{{hogehoge}}</div>
    <div>{{items}}</div>
  </div>
</template>

<script>
import $axios from 'axios';

export default {
  data() {
    return {
      hogehoge: "適当",
      items: []
    }
  },
  mounted() {
    this.hoge()
  },
  methods: {
    async hoge() {
      const url = "http://localhost:3000/books";
      const response = await $axios.get(url)
      this.items.push(response)
    }
  }
}
</script>
