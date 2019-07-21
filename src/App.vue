<template>
<div id="app">
    <div id="app_img"><img alt="Vue logo" src="./assets/logo.png"></div>
    
    <ToDoList msg="Vue To Do List"/>
</div>
</template>

<script>
import ToDoList from './components/to_do_list.vue';
export default {
    name: 'app',
    components: {
        ToDoList
    }
}
</script>

<style>
@import url('./static_css/app.css');
</style>