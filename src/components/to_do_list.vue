<template>
<div id="to_do_list">
    <h2>{{msg}}</h2>
    <p>
        <em>Simple Todo List with adding and filter by diff status.</em>
    </p>
    <ToDoInput v-on:add_item="add_item"/>
    <ToDoOutput v-bind:list="list"/>
    <ToDoOption />
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
            list: new Array()
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
        }
    }
}
</script>
