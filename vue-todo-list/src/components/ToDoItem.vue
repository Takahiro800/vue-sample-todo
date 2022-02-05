<template>
  <li class="todo-item" v-bind:class="{ done: done }" v-on:click="handleClick">
    <span v-if="done">✔︎</span> {{ text }}
  </li>
</template>

<script>
export default {
  // ToDoのコンテンツを指定するProp
  props: {
    text: {
      type: String,
    },
    done: {
      type: Boolean,
    },
  },
  emits: ['toggle'],
  methods: {
    // <li>のクリックイベントを処理
    handleClick() {
      this.$emit('toggle');
    },
  },
};
</script>
