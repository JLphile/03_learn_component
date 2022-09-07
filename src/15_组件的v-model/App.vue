<template>
  <div>
    <!-- <input :value="message" @input="message = $event.target.value" /> -->
    <!-- <input v-model="message" /> -->

    <!-- 组件绑定v-model -->
    <!-- <hy-input v-model="message"></hy-input> -->
    <!-- <hy-input
      :modelValue="message"
      @update:model-value="message = $event"
    ></hy-input> -->

    <!-- 绑定多个v-model -->
    <hy-input v-model="message" v-model:title="title"></hy-input>

    <h2>{{ message }}</h2>
    <h2>{{ title }}</h2>
  </div>
</template>

<script>
import HyInput from './HyInput.vue';
export default {
  components: {
    HyInput,
  },
  data() {
    return {
      message: 'Hello App',
      title: 'I am title',
    };
  },
};
</script>

<style scoped></style>
