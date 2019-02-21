<template>
                               <!-- binding a class to a condition with v-bind:class:"'className': prop" -->
    <section class="todo-item" v-bind:class="{'is-complete': todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{todo.title}} - {{ todo.completed}}
            <button @click="$emit('del-todo', todo.id)" class="delete">x</button>
        </p>
    </section>
</template>

<script>
export default {
    name: "TodoItem",
    props: [
        "todo" 
    ],
    methods: {
        markComplete() {
            this.todo.completed = !this.todo.completed;
        }
    } 
}
</script>

<style scoped>
    .todo-item {
        background-color: #ccc;
        padding: 8px;
        border-bottom: 1px dotted #fff;
    }
    .is-complete {
        text-decoration: line-through;
    }
    .delete {
        background-color: red;
        color: #fff;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }
</style>

