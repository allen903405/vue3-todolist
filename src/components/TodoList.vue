<template>
    <h1>Todolist</h1>
    <todo-form @send-message="createTodo"></todo-form>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import TodoForm from './TodoForm.vue'
@Options({
    components: {
        TodoForm,
    }
})
export default class TodoList extends Vue {
    async createTodo(todo){
        console.log("TodoList", todo)
        alert("TodoList created")
    }
}
</script>