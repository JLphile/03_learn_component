<template>
  <div>
    <!-- 绑定到一个元素上 -->
    <h2 ref="title">App组件内容</h2>

    <!-- 绑定到组件实例上 -->
    <nav-bar ref="navBar"></nav-bar>

    <button @click="btnClick">我是按钮</button>
  </div>
</template>

<script>
import NavBar from './NavBar.vue';
export default {
  components: {
    NavBar,
  },
  data() {
    return {
      names: ['Peter', 'Tom'],
    };
  },
  methods: {
    btnClick() {
      console.log(this.$refs);

      console.log(this.$refs.title);
      console.log(this.$refs.navBar.message);
      this.$refs.navBar.sayHello();
      // $el 获取根元素
      console.log(this.$refs.navBar.$el);
    },
  },
};
</script>

<style scoped></style>
