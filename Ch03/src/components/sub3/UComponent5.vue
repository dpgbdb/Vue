<template>
  <h4>UComponent5</h4>
  <p>
    이름 : <input type="text" v-model="name" /><br />
    나이 : <input type="text" v-model="age" /><br />
  </p>
  <button @click="btnSandData">상위 컴포넌트로 데이터 전달</button>
</template>
<script>
export default {
  name: "UComponent5",
  data() {
    return {
      name: "",
      age: 0,
    };
  },
  methods: {
    btnSandData: function () {
      let data = {
        name: this.name,
        age: this.age,
      };
      this.$emit("myShow", data);
    },
  },
};
</script>
<style scoped></style>
