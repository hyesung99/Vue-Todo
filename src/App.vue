<template>
  <h1>Simple Vue Todo</h1>
  <TodoInput @change="changeValue" @submit="addTodo" />
  <Todo :todos="todos" />
</template>

<script>
import * as TodoComponents from '~/components/index'
import TodoInput from './components/TodoInput.vue'

export default {
  components: { ...TodoComponents, TodoInput },
  data() {
    return {
      todoValue: '',
      todos: [],
    }
  },
  methods: {
    changeValue(newTodoValue) {
      this.todoValue = newTodoValue
    },
    addTodo(newValue) {
      const value = newValue || this.todoValue
      this.todos.push({
        id: Date.now(),
        value,
      })
      this.todoValue = ''
    },
  },
}
</script>

<style scoped lang="scss"></style>
