<template>
  <div class="container">
    <todo-list></todo-list>
    <todo-form></todo-form>
  </div>
</template>
<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import TodoList from './components/TodoList.vue'
import TodoForm from './components/TodoForm.vue'

@Options({
  components: {
    TodoList,
    TodoForm,
  },
})
export default class App extends Vue {}
</script>


<style lang="scss">
body{
  margin: 0;
}
.container{
  background-color: #e9eef3;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
