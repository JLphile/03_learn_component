<template>
  <div>
    <h2>NavBar内容</h2>
    <button @click="getParentAndRoot">获取parent和root对象</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'I am the message of the NavBar',
    };
  },
  methods: {
    sayHello() {
      console.log('hello navbar');
    },
    getParentAndRoot() {
      console.log(this.$parent);
      console.log(this.$root);
    },
  },
};
</script>

<style scoped></style>
