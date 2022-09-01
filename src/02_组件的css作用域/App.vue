<template>
  <h2>App</h2>
  <hello-word></hello-word>
</template>

<script>
import HelloWord from './HelloWord.vue';
export default {
  components: {
    HelloWord,
  },
};
</script>

<style scoped>
h2 {
  color: red;
}
</style>
