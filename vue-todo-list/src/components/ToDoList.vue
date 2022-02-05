<template>
  <div>
    <input v-model="inputValue" />
    <button v-on:click="handleClick">TODOを追加</button>
    <ul>
      <li v-for="todo in todoItems" v-bind:key="todo.id">
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
        { id: 1, text: 'Go out to sea' },
        { id: 2, text: 'Invite the first member' },
      ],
    };
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
