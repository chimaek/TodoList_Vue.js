<template>
  <div id="app">
    <todo-header></todo-header>
    <todo-input></todo-input>
    <todo-list></todo-list>
    <todo-footer></todo-footer>
  </div>
</template>
<script>
import TodoFooterVue from "./components/TodoFooter.vue";
import TodoHeaderVue from "./components/TodoHeader.vue";
import TodoInputVue from "./components/TodoInput.vue";
import TodoListVue from "./components/TodoList.vue";

export default {
  components: {
    TodoHeader: TodoHeaderVue,
    TodoInput: TodoInputVue,
    TodoList: TodoListVue,
    TodoFooter: TodoFooterVue,
  },
};
</script>

<style>
/* @import url("https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css");
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.8.2/css/all.min.css"); */
body {
  text-align: center;
  background-color: #f6f6f8;
}
input {
  border-style: groove;
  width: 200px;
}
button {
  border-style: groove;
}
.shadow {
  box-shadow: 5px 10px 10px rgba(0, 0, 0, 0.03);
}
</style>