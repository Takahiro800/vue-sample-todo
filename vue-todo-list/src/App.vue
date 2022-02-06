<template>
  <!-- ToDoListを使用する -->
  <div>
    <ToDoList />
    <ComponentSample />
    <Slot />
    <ScopSlot>
  </div>
</template>

<script>
import ComponentSample from './components/Component.vue';
import ToDoList from './components/ToDoList.vue';
import Slot from './components/Slot.vue';
import ScopSlot from './components/ScopSlot.vue'
export default {
  name: 'App',
  // ToDoListを<template>で使用できるようにする
  components: {
    ToDoList,
    ComponentSample,
    Slot,
    ScopSlot
  },
};
</script>
