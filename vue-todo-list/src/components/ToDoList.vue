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
    filterdTodoItems() {
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
