<template>
  <h4>Query</h4>
  <p>
    user : {{ user }}<br />
    uid : {{ user.uid }}<br />
    name : {{ user.name }}<br />
    age : {{ user.age }}<br />
  </p>
</template>
<script setup>
import { useRoute } from "vue-router";

const route = useRoute();
const user = route.query;
</script>
<style scoped></style>
