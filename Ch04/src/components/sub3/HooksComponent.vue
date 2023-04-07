<template>
  <h4>HooksComponent</h4>
  <p>
    카운트 : {{ count }}
    <button @click="btnCountUp">증가</button>
  </p>
</template>
<script setup>
import { ref } from "vue";
import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
} from "vue";

const count = ref(0);

const btnCountUp = () => {
  count.value++;
};
//Hooks
onBeforeMount(() => {
  console.log("onBeforeMount...");
});

onMounted(() => {
  console.log("onMount...");
});

onBeforeUpdate(() => {
  console.log("onBeforeUpdate...");
});

onUpdated(() => {
  console.log("onUpdate...");
});
onBeforeUnmount(() => {
  console.log("onBeforeUnMount...");
});
onUnmounted(() => {
  console.log("onUnMount...");
});
</script>
<style scoped></style>
