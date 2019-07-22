<template>
<div id="app">
    <div id="app_img"><img alt="Vue logo" src="./assets/logo.png"></div>
    <div id="container">
        <Header msg="Vue To Do List" />

        <Body :list="list" :output="output" />
        <Footer @all="all" @active="active" @complete="complete"/>
    </div>
</div>
</template>

<script>
import Header from "./components/header.vue";
import Body from './components/body.vue';
import Footer from './components/footer.vue';
export default {
    name: 'app',
    data: () => {
        return {
            list: new Array(),
            output: new Array(),
        }
    },
    components: {
        Header,
        Body,
        Footer
    },
    methods: {
        all: function () {
            this.output = JSON.parse(JSON.stringify(this.list));
        },
        active: function () {
            this.output.length == this.list.length ? this.list = this.output : "";
            this.output = this.list.filter(i => !i.key);
        },
        complete: function () {
            this.output.length == this.list.length ? this.list = this.output : "";
            this.output = this.list.filter(i => i.key);
        }
    }
}
</script>

<style>
@import url('./static_css/app.css');
</style>
