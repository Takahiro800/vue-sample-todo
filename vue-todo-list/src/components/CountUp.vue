<template>
  <button v-on:click="handleClick">+1</button>
</template>
<script>
export default {
  inject: ['counterContainer'],
  methods: {
    handleClick() {
      const container = this.counterContainer;
      container.count++;
    },
  },
};
</script>
