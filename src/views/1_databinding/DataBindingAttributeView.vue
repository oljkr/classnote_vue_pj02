<template>
  <div>
    <h2>다양한 속성 바인딩</h2>
    <hr>
    <h3>readonly 속성</h3>
    <input type="text" name="" id="" v-model="userId" readonly>
    <br>
    <input type="text" name="" id="" v-bind:value="userId" readonly>
    <br>
    <input type="text" name="" id="" :value="userId" readonly>

    <h3>src 속성</h3>
    <img v-bind:src="imgSrc" alt="" style="width: 100px; height:auto">
    <hr>

    <h3>disabled 속성</h3>
    <input type="search" name="" id="" v-model="txt1">
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userId: 'Korea',
      imgSrc: 'https://www.itwill.co.kr/css/wvtex/img/wvUser/logo.png',
      txt1: ''
    }
  }
}
</script>
