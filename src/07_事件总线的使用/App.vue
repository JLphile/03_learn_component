<template>
  <div>
    <home></home>
    <about-vue></about-vue>
  </div>
</template>

<script>
import Home from './Home.vue';
import AboutVue from './About.vue';

export default {
  components: {
    Home,
    AboutVue,
  },
};
</script>

<style scoped></style>
