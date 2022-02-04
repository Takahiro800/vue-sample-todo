<template>
  <!-- ToDoListを使用する -->
  <ToDoList />
</template>

<script>
import ToDoList from './components/ToDoList.vue';
export default {
  name: 'App',
  // ToDoListを<template>で使用できるようにする
  components: {
    ToDoList,
  },
};
</script>
