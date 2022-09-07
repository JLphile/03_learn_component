<template>
  <div>
    <!-- <input :value="message" @input="message = $event.target.value" /> -->
    <!-- <input v-model="message" /> -->

    <!-- 组件绑定v-model -->
    <hy-input v-model="message"></hy-input>
    <!-- <hy-input
      :modelValue="message"
      @update:model-value="message = $event"
    ></hy-input> -->

    <h2>{{ message }}</h2>
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
    };
  },
};
</script>

<style scoped></style>
