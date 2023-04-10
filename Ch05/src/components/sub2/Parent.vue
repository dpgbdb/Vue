<template>
  <div>
    <h4>Parent</h4>
    <RouterLink to="/parent/child1">child1</RouterLink>
    <RouterLink to="/parent/child2">child2</RouterLink>

    <router-view></router-view>
  </div>
</template>
<script>
export default {
  name: "Parent",
  setup() {
    return {};
  },
};
</script>
<style scoped>
div {
  border: 1px solid red;
}
</style>
