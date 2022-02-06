<template>
  <ChildComponent>
    <template v-slot:default="{ foo }">
      <p>{{ foo }}</p>
    </template>
  </ChildComponent>
</template>

<script>
import ChildComponent from './ScopSlotChild.vue';
export default {
  components: { ChildComponent },
};
</script>
