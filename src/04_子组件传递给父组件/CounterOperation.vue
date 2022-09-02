<template>
  <div>
    <button @click="increment">+1</button>
    <button @click="decrement">-1</button>
    <input type="text" v-model.number="num" />
    <button @click="incrementN">+n</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
    };
  },
  //   emits: ['add', 'sub', 'addN'],
  emits: {
    add: null,
    sub: null,
    addN: (num, name, age) => {
      console.log(num, name, age);
      if (num > 10) {
        return true;
      }
      return false;
    },
  },
  methods: {
    increment() {
      console.log('+1');
      this.$emit('add');
    },
    decrement() {
      console.log('-1');
      this.$emit('sub');
    },
    incrementN() {
      this.$emit('addN', this.num);
    },
  },
};
</script>

<style scoped></style>
