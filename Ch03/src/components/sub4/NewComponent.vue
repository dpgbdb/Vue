<template>
  <h4>NewComponent</h4>
  <p>카운터 : {{ count }}</p>
  <button @click="countOne">증가</button>
</template>
<script>
export default {
  name: "NewComponent",
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    countOne: function () {
      this.count++;
    },
  },
  beforeCreate: function () {
    console.log("beforeCreate...");
  },
  created: function () {
    console.log("Created...");
  },
  beforeMount: function () {
    console.log("beforeMount...");
  },
  mounted: function () {
    console.log("Mounted...");
  },
  beforeUpdate: function () {
    console.log("beforeUpdate...");
  },
  updated: function () {
    console.log("Updated...");
  },
  beforeUnmount: function () {
    console.log("beforeUnmount...");
  },
  unmounted: function () {
    console.log("Unmounted...");
  },
};
</script>
<style scoped></style>
