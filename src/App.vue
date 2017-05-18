<template>
  <div id="app">
    <Header></Header>
    <TodoList></TodoList>
  </div>
</template>

<script>
import Header from '@/components/Header';
import TodoList from '@/components/TodoList';

export default {
  name: 'app',
  components: {
    Header,
    TodoList,
  },
};
</script>

<style>
body, html {
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
}
</style>
