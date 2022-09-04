<template>
  <div>
    <button @click="btnClick">about按钮点击</button>
  </div>
</template>

<script>
import emitter from './utils/eventbus';
export default {
  methods: {
    btnClick() {
      console.log('about按钮点击了');
      emitter.emit('why', { name: 'why', age: 18 });
      //   emitter.emit('kobe', { name: 'kobe', age: 33 });
    },
  },
};
</script>

<style scoped></style>
