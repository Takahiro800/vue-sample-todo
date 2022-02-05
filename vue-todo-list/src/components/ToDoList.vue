<template>
  <div>
    <div>
      <input v-model="inputValue" />
      <button v-on:click="handleClick">TODOを追加</button>
    </div>
    <input v-model="filterValue" placeholder="フィルタテキスト" />
    <ul>
      <ToDoItem
        v-for="todo in filteredTodoItems"
        v-bind:key="todo.id"
        v-bind:text="todo.text"
        v-bind:done="todo.done"
      />
    </ul>
  </div>
</template>

<script>
import ToDoItem from './ToDoItem.vue';
export default {
  components: { ToDoItem },
  data() {
    return {
      inputValue: '',
      todoItems: [
        { id: 1, done: false, text: 'Go out to sea' },
        { id: 2, done: true, text: 'Invite the first member' },
      ],
      filterValue: '',
    };
  },
  computed: {
    filteredTodoItems() {
      if (!this.filterValue) {
        return this.todoItems;
      }
      return this.todoItems.filter((todo) => {
        return todo.text.includes(this.filterValue);
      });
    },
  },
  methods: {
    handleClick() {
      this.todoItems.push({
        id: this.todoItems.length + 1,
        text: this.inputValue,
      });
      this.inputValue = '';
    },
  },
};
</script>

<style>
.todo-item.done {
  background-color: #3fb983;
  color: #ffffff;
}
</style>
