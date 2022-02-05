<template>
  <!-- ToDoListを使用する -->
  <div>
    <ToDoList />
    <test />
  </div>
</template>

<script>
import test from './components/Component.vue';
import ToDoList from './components/ToDoList.vue';
export default {
  name: 'App',
  // ToDoListを<template>で使用できるようにする
  components: {
    ToDoList,
    test,
  },
};
</script>
