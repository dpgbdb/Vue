<template>
  <h4>Options API - methods</h4>
  <button v-on:click="btn1Click">button1</button>
  <button v-on:click="btn2Click">button2</button>
  <button @click="btn3Click">button3</button>
</template>
<script>
export default {
  name: "ApiComponent2",
  // 이벤트 처리와 로직 제어에 관련한 함수를 정의하는 API
  methods: {
    btn1Click() {
      alert("button1 click!");
    },
    btn2Click: function () {
      alert("button2 click!");
    },
    btn3Click: () => {
      alert("button3 click!");
    },
  },
};
</script>
<style scoped></style>
