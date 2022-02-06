<template>
  <CounterProvider>
    <CountUp />
    <RenderCount />
  </CounterProvider>
</template>

<script>
import CounterProvider from './CounterProvider.vue';
import RenderCount from './RenderCount.vue';
import CountUp from './CountUp.vue';
export default {
  components: {
    CounterProvider,
    RenderCount,
    CountUp,
  },
};
</script>
