<template>
  <div class="container">
    <p><button @click="getList">목록</button></p>
    <ul class="list-group">
      <li v-if="memoList.length == 0" class="list-group-item">게시물이 없습니다<br>
      <img src="../../assets/kuromi68.jpg" class="image">
      </li>
      <li v-for="memo in memoList" v-bind:key="memo.memono" class="list-group-item">{{ memo.subject }}<span class="badge">{{ memo.readcnt }}</span></li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      memoList: []
    }
  },
  methods: {
    getList() {
      // alert()
      // fetch(요청명령어).then(응답메세지).then(출력)
      fetch('http://localhost:9000/memolist')
        .then((response) => {
          if (response.ok) {
            // alert(response)
            // alert(response.json())
            return response.json()
          }
        }).then((json) => {
          // alert(json)
          this.memoList = json
        })
    }
  }
}
</script>

<style scoped>
@import 'https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css';
.image {
  width: 300px;
}
</style>
