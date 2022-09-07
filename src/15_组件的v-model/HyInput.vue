<template>
  <div>
    <!-- 1.默认绑定和事件处理 -->
    <!-- <button @click="btnClick">HyInput按钮</button>
    <h2>HyInput的message:{{ modelValue }}</h2> -->

    <!-- 2.通过input -->
    <!-- <input type="text" :value="modelValue" @input="btnClick" /> -->

    <!-- 3.绑定到props中是不对的 -->
    <!-- <input type="text" v-model="modelValue"> -->

    <!-- 4.通过computed来完成绑定 -->
  </div>
</template>

<script>
export default {
  props: {
    modelValue: String | Number,
  },
  emits: ['update:modelValue'],
  methods: {
    btnClick(event) {
      this.$emit('update:modelValue', event.target.value);
    },
  },
};
</script>

<style scoped></style>
