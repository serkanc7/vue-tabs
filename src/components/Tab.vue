<template>
  <h1>{{ content.title }}</h1>
  <p>{{ content.text }}</p>
</template>

<script>
export default {
  props: ["content"],
  setup() {},
};
</script>

<style>
</style>