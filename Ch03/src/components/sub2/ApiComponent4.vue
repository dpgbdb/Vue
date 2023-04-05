<template>
  <h4>Options API - watch</h4>
  <p>금지문자 : {{ banText }}</p>
  <textarea v-model="inputText"></textarea>
</template>
<script>
export default {
  name: "ApiComponent4",
  data() {
    return {
      banText: "stupid",
      inputText: "",
    };
  },
  watch: {
    inputText: function () {
      console.log("inputText watch!!!");

      let pos = this.inputText.indexOf(this.banText);
      if (pos >= 0) {
        alert(this.banText + " 는 입력 불가!");
        this.inputText = this.inputText.substring(0, pos);
      }
    },
  },
};
</script>
<style scoped></style>
