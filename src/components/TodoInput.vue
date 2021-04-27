<template>
  <div class="inputbox shadow">
    <input type="text" v-model="newTodoItem" placeholder="할 일을 입력하세요!" v-on:keyup.enter='addTodo'/>
    <span class="addContainer" v-on:click="addTodo">
        <i class="addBtn fa fa-plus" aria-hidden="true">
        </i>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoItem: "",
    };
  },
  methods: {
    addTodo: function () {
      if (this.newTodoItem !== "") {
        var value = this.newTodoItem && this.newTodoItem.trim();
        localStorage.setItem(value, value);
        this.clearInput();
      } else {
        alert("문자를 입력하세여!");
      }
    },
    clearInput: function () {
      this.newTodoItem = "";
    },
  },
};
</script>

<style scoped>
    input:focus{
        outline: none;
    }
    .inputbox{
        background: white;
        height: 50px;
        line-height: 50px;
        border-radius: 5px;
    }
    .inputbox input{
        border-style: none;
        font-size: 0.9rem;
    }
    .addContainer{
        float: right;
        background: linear-gradient(to right,#6486fb,#8763fb);
        display: inline-block;
        width: 3rem;
        border-radius: 0 5px 5px 0;
    }
    .addBtn{
        color: white;
        vertical-align: middle;
    }
</style>