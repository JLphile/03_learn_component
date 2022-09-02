<template>
  <h2>MulitRootElement</h2>
  <h2 :id="$attrs.id">MulitRootElement</h2>
  <h2>MulitRootElement</h2>
</template>

<script>
export default {
  props: {
    title: String,
    content: {
      type: String,
      require: false,
    },
  },
};
</script>

<style scoped></style>
