<template>
  <show-message-vue
    title="父传子title"
    content="父传子content"
    class="why"
  ></show-message-vue>
  <show-message-vue
    title="第二次父传子title"
    content="第二次父传子content"
  ></show-message-vue>
  <show-message-vue :title="title" :content="content"></show-message-vue>
  <show-message-vue
    :title="message.title"
    :content="message.content"
  ></show-message-vue>
  <show-message-vue v-bind="message"></show-message-vue>
  <mulit-root-element id="my-id"></mulit-root-element>
</template>

<script>
import ShowMessageVue from './ShowMessage.vue';
import MulitRootElement from './MulitRootElement.vue';
export default {
  components: {
    ShowMessageVue,
    MulitRootElement,
  },
  data() {
    return {
      title: 'data父传子',
      content: 'data父传子content',
      message: {
        title: 'object-title',
        content: 'object-content',
      },
    };
  },
};
</script>

<style scoped></style>
