<template>
  <slot />
</template>

<script>
export default {
  data() {
    return {
      container: { count: 0 },
    };
  },
  provide() {
    const counterContainer = this.container;
    return { counterContainer };
  },
};
</script>
