<template>
  <div>
    <button @click="increaseCounter">좋아요</button>
    <p>{{ counter }}</p>
    <img src="../../assets/kuromi7.jpg" class="image">
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increaseCounter() {
      this.counter += 1
    }
  }
}
</script>

<style scoped>
.image {
  width: 300px;
}
</style>
