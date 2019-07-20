<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <ToDoList msg="Vue To Do List"/>
  </div>
</template>

<script>
import ToDoList from './components/to_do_list.vue';
export default {
  name: 'app',
  components:{ToDoList}
}
</script>

<style>
  @import url('./static_css/app.css');
</style>