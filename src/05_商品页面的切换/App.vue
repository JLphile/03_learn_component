<template>
  <div>
    <tab-control-vue
      :titles="titles"
      @titleClick="titleClick"
    ></tab-control-vue>
    <h2>{{ contents[currentIndex] }}</h2>
  </div>
</template>

<script>
import TabControlVue from './TabControl.vue';
export default {
  components: {
    TabControlVue,
  },
  data() {
    return {
      titles: ['衣服', '鞋子', '帽子'],
      contents: ['衣服页面', '鞋子页面', '帽子页面'],
      currentIndex: 0,
    };
  },
  methods: {
    titleClick(index) {
      this.currentIndex = index;
    },
  },
};
</script>

<style scoped></style>
