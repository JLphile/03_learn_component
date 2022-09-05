<template>
  <div>
    <nav-bar :name="name">
      <!-- v-slot:可以用#替代 -->
      <template v-slot:left>
        <button>左边的按钮</button>
      </template>
      <template #center>
        <h3>中间标题</h3>
      </template>
      <template #right>
        <i>右边的i元素</i>
      </template>
      <template #[name]>
        <i>why的内容</i>
      </template>
    </nav-bar>
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
      name: 'why',
    };
  },
};
</script>

<style scoped></style>
