<template>
  <li class="todo-item" v-bind:class="{ done: done }"><span v-if="done">✔︎</span> {{ text }}</li>
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
};
</script>
