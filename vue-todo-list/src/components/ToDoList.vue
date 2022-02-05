<template>
  <div>
    <input v-model="inputValue" />
    入力した値: {{ inputValue }}
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
};
</script>
