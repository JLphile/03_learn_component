<template>
  <div>
    <h2 :class="$attrs.class">{{ title }}</h2>
    <h2>{{ content }}</h2>
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  //   props: ['title', 'content'],
  props: {
    title: String,
    content: {
      type: String,
      required: false,
      default: 'content默认值',
    },
  },
};
</script>

<style scoped></style>
