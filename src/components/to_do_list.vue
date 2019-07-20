<template>
<div id="to_do_list">
    <h2>{{msg}}</h2>
    <p>
        <em>Simple Todo List with adding and filter by diff status.</em>
    </p>
    <ToDoInput v-on:add_item="add_item"/>
    <ToDoOutput v-bind:list="temp"/>
    <ToDoOption v-on:all="all" v-on:active="active" v-on:complete="complete"/>
</div>
</template>

<script>
import ToDoInput from './to_do_input.vue';
import ToDoOutput from './to_do_output.vue';
import ToDoOption from './to_do_option.vue';
export default {
    name: 'to_do_list',
    data:()=>{
        return{
            list: new Array(),
            temp: new Array(),
        }
    },
    props: {
        msg: String,
    },
    components: {
        ToDoInput,
        ToDoOutput,
        ToDoOption
    },
    methods:{
        add_item:function(item){
            this.list.push({key:false,value:item});
            this.temp.push({key:false,value:item});
        },
        all:function(){
            this.temp = this.list;
        },
        active:function(){
            this.temp = this.list.filter(i=>!i.key);
        },
        complete:function(){
            this.temp = this.list.filter(i=>i.key);
        }
    }
}
</script>
