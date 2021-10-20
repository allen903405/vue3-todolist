<template>
<!-- <h1>TodoList</h1> -->
<form @submit.prevent :inline="true" :model="formInput" class="todo-form-inpupt">

        <input type="text" class="col-md-6" v-model="formInput.title" placeholder="Enter Todo">

        <button type="button" class="btn btn-primary m-2" @click="onSubmit()">Add</button>

</form>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({})
export default class TodoForm extends Vue {
   formInput = { title: "", completed: false };
   
   onSubmit(){
    console.log("TodoForm", this.formInput)
    this.$emit('send-message', this.formInput)
   }
}
</script>