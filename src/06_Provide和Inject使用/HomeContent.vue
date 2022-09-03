<template>
  <div>HomeContent的内容: {{ name }}-{{ age }}-{{ length }}</div>
</template>

<script>
export default {
  inject: ['name', 'age', 'length'],
};
</script>

<style scoped></style>
