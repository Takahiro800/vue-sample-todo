<template>
  <!-- ToDoListを使用する -->
  <div>
    <ToDoList />
    <ComponentSample />
    <Slot />
  </div>
</template>

<script>
import ComponentSample from './components/Component.vue';
import ToDoList from './components/ToDoList.vue';
import Slot from './components/Slot.vue';
export default {
  name: 'App',
  // ToDoListを<template>で使用できるようにする
  components: {
    ToDoList,
    ComponentSample,
    Slot,
  },
};
</script>
