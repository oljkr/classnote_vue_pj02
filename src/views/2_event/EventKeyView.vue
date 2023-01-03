<template>
  <div>
    <input type="search" @keyup="checkEnter($event)" v-model="searchText">
    <hr>
    <input type="search" @keyup.enter="doSearch" v-model="searchText">
    <button @click="doSearch">조회</button><br><br>
    <img src="../../assets/kuromi17.jpg" class="image">
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchText: ''
    }
  },
  methods: {
    doSearch() {
      alert(this.searchText)
    },
    checkEnter() {
      // alert(event)
      if (event.keyCode === 13) {
        // alert('hello world')
        this.doSearch()
      }
    }
  }
}
</script>

<style scoped>
.image {
  width: 300px;
}
</style>
