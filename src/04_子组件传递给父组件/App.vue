<template>
  <h2>当前计数：{{ counter }}</h2>
  <counter-operation-vue
    @add="addOne"
    @sub="subOne"
    @addN="addNNum"
  ></counter-operation-vue>
</template>

<script>
import CounterOperationVue from './CounterOperation.vue';
export default {
  components: {
    CounterOperationVue,
  },
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    addOne() {
      this.counter++;
    },
    subOne() {
      this.counter--;
    },
    addNNum(num) {
      this.counter += num;
    },
  },
};
</script>

<style scoped></style>
