<template>
  <div>
    <div>{{items}}</div>
  </div>
</template>

<script>
import $axios from 'axios';

export default {
  data() {
    return {
      items: ""
    }
  },
  mounted() {
    this.hoge()
  },
  methods: {
    async hoge() {
      const url = "http://localhost:3000/books";
      const response = await $axios.get(url)
      this.items = response.data
    }
  }
}
</script>
