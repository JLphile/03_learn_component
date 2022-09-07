<template>
  <div>
    App组件
    <home></home>
    <suspense>
      <template #default>
        <async-category></async-category>
      </template>
      <template #fallback>
        <loading></loading>
      </template>
    </suspense>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue';
import Home from './Home.vue';
import Loading from './Loading.vue';
// import AsyncCategory from './AsyncCategory.vue';
const AsyncCategory = defineAsyncComponent(() => import('./AsyncCategory.vue'));
// const AsyncCategory = defineAsyncComponent({
//   loader: () => import('./AsyncCategory.vue'),
//   loadingComponent: Loading,
//   errorComponent: Error,
//   // 在显示loadingComponent 组件之前等待多长时间
//   delay: 2000,
// /**
//  * err：错误信息，
//  * retry：函数，调用retry函数重新加载
//  * fail()函数
//  * attempts：记录尝试的次数
//  */
//   onError: function (err, retry,fail, attempts) {},
// });

export default {
  components: {
    Home,
    AsyncCategory,
    Loading,
  },
};
</script>

<style scoped></style>
