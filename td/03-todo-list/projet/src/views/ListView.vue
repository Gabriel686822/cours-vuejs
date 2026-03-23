<script setup lang="js">
import todos from '@/assets/todos.js'
import Button from '@/components/DesignedButton.vue';
import TodoCreation from '@/components/todo/TodoCreation.vue'
import TodoList from '@/components/todo/TodoList.vue';
import {ref} from 'vue';

const todoList = ref(todos);
</script>

<template>
  <div class="list-view">
    <h2>List</h2>
    <TodoList :todos="todoList" />
    <TodoCreation @creation="(todo) => {
      todo.id = todoList.length +1;
      todoList.push(todo)}"/>
  </div>
</template>

<style lang="css" scoped>
.list-view {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

h2 {
  font-size: 1.5em;
}
</style>
