<template>
  <div>
    <input v-model="inputValue" />
    <button v-on:click="handleClick">TODOを追加</button>
    <input v-model="filterValue" placeholder="フィルタテキスト" />
    <ul>
      <li v-for="todo in filterdTodoItems" v-bind:key="todo.id" v-on:click="todo.done = !todo.done">
        <span v-if="todo.done">✅</span>
        {{ todo.text }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    const todoItems = [
      { id: 1, done: false, text: 'Go out to sea' },
      { id: 2, done: true, text: 'Invite the first member' },
    ];
    return {
      inputValue: '',
      todoItems,
      filterdTodoItems: todoItems,
      filterValue: '',
    };
  },
  watch: {
    // filterValueの値の変更を監視し、filterdTodoItemsを再計算する
    filterValue() {
      this.updateFilteredTodoItems();
    },
    todoItems: {
      handler() {
        this.updateFilteredTodoItems();
      },
      deep: true,
    },
  },
  methods: {
    updateFilteredTodoItems() {
      this.filterValue ? this.todoItems.filter((todo) => todo.text.includes(this.filterValue)) : this.todoItems;
    },
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
