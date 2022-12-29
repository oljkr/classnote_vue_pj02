<template>
  <div>
    <h1>Hello {{ userName }}</h1>
    <p>{{ message }}</p>
    <h2>환영합니다</h2>
    💖🤍🎀🌸💖🤍🎀🌸💖🤍🎀🌸💖🤍🎀🌸💖
    <img src="../../assets/kuromi5.jpg">
  </div>
</template>

<script>
export default {
  data() {
    return {
      userName: 'John Doe',
      message: '서울특별시'
    }
  }
}
</script>
