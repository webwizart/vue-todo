<template>
  <section>
    <div
      v-for="todo in todos"
      v-bind:key="todo.id">
        <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
    </div>
  </section>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "Todos",
  components: {
    TodoItem
  },
  props: ["todos"]
};
</script>

<style scoped>
.todo {
  background-color: deeppink;
}
</style>

