<template>
  <div>
    <Home></Home>
    <button @click="addName">添加名字</button>
  </div>
</template>

<script>
import Home from './Home.vue';
import { computed } from 'vue';

export default {
  components: {
    Home,
  },
  provide() {
    return {
      name: 'why',
      age: 18,
      length: computed(() => this.names.length),
    };
  },
  data() {
    return {
      names: ['aaa', 'bbb', 'ccc', 'ddd'],
    };
  },
  methods: {
    addName() {
      this.names.push('why');
      console.log(this.names);
    },
  },
};
</script>

<style scoped></style>
