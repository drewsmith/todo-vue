<template>
  <div id="todo-list">
    <div id="add-wrapper">
      <input type="text" v-model="new_todo" placeholder="Enter TODO and press return" v-on:keyup="addTodo">
    </div>
    <ul>
      <li v-for="(todo, index) in todos">
        {{todo}}
        <span class="remove" v-on:click="removeTodo(index)">Remove</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  data() {
    return {
      todos: [
      ],
      new_todo: '',
    };
  },
  methods: {
    addTodo(e) {
      if (e.keyCode !== 13) {
        return;
      }
      if (this.new_todo) {
        this.todos.push(this.new_todo.trim());
        this.new_todo = '';
      }
    },
    removeTodo(index) {
      this.todos.splice(index, 1);
    },
  },
};
</script>

<style scoped>
input[type="text"] {
  width: 94%;
  font-size: 24px;
  color: #333;
  padding: 10px 20px;
  border:1px solid #e9e9e9;
  outline: 0;
  border-radious: 10px;
  -moz-border-radius: 10px;
  -webkit-border-radius: 10px;
  box-shadow: 2px 2px #e1e1e1;
}
button {
  font-size: 14px;
  background: #333;
  color: #e9e9e9;
  padding: 8px 16px;
  text-transform: uppercase;
  border: 0;
  box-shadow: 2px 2px 0 #000;
  border-radious: 4px;
  -moz-border-radius: 4px;
  -webkit-border-radius: 4px;
  margin-left: 10px;
  cursor: pointer;
}
ul {
  margin: 20px;
  padding: 0;
}
li {
  list-style-type: none;
  margin: 0 0 20px 0;
  padding: 10px 20px;
  background: #f9f9f9;
  box-shadow: 2px 2px 0 #e9e9e9;
  text-shadow: 0 1px 0 #ffffff;
  color: #333;
  font-weight: 300;
  font-size: 20px;
  text-align: left;
  border-radious: 10px;
  -moz-border-radius: 10px;
  -webkit-border-radius: 10px;
}
.remove {
  font-weight: 600;
  font-size: 10px;
  text-transform: uppercase;
  cursor: pointer;
  background: #C11111;
  color: #ffffff;
  padding: 6px 12px;
  float: right;
  border-radious: 4px;
  -moz-border-radius: 4px;
  -webkit-border-radius: 4px;
  box-shadow: 2px 2px 0 #630000;
  text-shadow: 0 1px 0 #630000;
}
::-webkit-input-placeholder {
  color: #d9d9d9;
}
::-moz-placeholder {
  color: #d9d9d9;
}
:-ms-input-placeholder {
  color: #d9d9d9;
}
:-moz-placeholder {
  color: #d9d9d9;
}
</style>
