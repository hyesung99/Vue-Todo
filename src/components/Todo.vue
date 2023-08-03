<template>
  <ul>
    <li v-for="todo in todos">
      <p>{{ todo.value }}</p>
    </li>
  </ul>
</template>
<script>
export default {
  props: {
    todos: {
      type: Array,
      default: [],
    },
  },
}
</script>
