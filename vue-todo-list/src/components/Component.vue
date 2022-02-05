<template>
  <ChildComponent v-bind:count="myCount" v-on:update="handleUpdate" />
</template>
<script>
import ChildComponent from './ChildComponent.vue';
export default {
  components: { ChildComponent },
  data() {
    return { myCount: 0 };
  },
  methods: {
    handleUpdate(newCount) {
      this.myCount = newCount;
    },
  },
};
</script>
