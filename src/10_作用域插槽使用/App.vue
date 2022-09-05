<template>
  <div>
    <!-- {{title}} 不能引入子组件中的数据-->
    <!-- <child-cpn-vue>
      <button>{{title}}</button>
    </child-cpn-vue> -->
    <show-names-vue :names="names">
      <template v-slot="slotProps">
        <button>{{ slotProps.item }}-{{ slotProps.index }}</button>
      </template>
    </show-names-vue>

    <!-- 如果还有其他的具名插槽，那么必须采用template包裹的形式书写 -->
    <show-names-vue :names="names">
      <template v-slot="slotProps">
        <strong>{{ slotProps.item }}-{{ slotProps.index }}</strong>
      </template>
    </show-names-vue>
    <!-- 独占默认插槽的缩写 -->
    <show-names-vue :names="names" v-slot="coderwhy">
      <strong>{{ coderwhy.item }}-{{ coderwhy.index }}</strong>
    </show-names-vue>
  </div>
</template>

<script>
import ChildCpnVue from './ChildCpn.vue';
import ShowNamesVue from './ShowNames.vue';
export default {
  components: {
    ChildCpnVue,
    ShowNamesVue,
  },
  data() {
    return {
      names: ['why', 'kobe', 'james', 'curry'],
    };
  },
};
</script>

<style scoped></style>
