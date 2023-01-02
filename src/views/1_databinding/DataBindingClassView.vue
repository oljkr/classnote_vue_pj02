<template>
  <div>
    <div :class="{'text-red':true}">클래스 바인딩1</div>
    <div :class="{'text-red':false}">클래스 바인딩2</div>
    <div :class="{'text-red':true, 'active':true }">클래스 바인딩3</div>
    <div :class="{'text-red':true, active:true }">클래스 바인딩4</div>
    <!--성택자명이 두개의 단어로 구성되어 있으면 ' 기호 생략시 에러
    <div :class="{ text-red:true }">클래스 바인딩4</div>
    -->
    <div :class="{'text-red':hasError, 'active':isActive }">클래스 바인딩5</div>
    <div :class="class2">클래스 바인딩6</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hasError: true,
      isActive: true,
      class2: ['active', 'text-red']
    }
  }
}
</script>

<style scoped>
.active { background-color: greenyellow; font-weight: bold; }
.text-red { color: red; }
</style>
