<template>
<div id="bbody">
    <InputBar @add_item="add_item"/>
    <ListContainer :list="output"/>
</div>
</template>

<script>
import InputBar from './input_bar.vue';
import ListContainer from './list_container.vue';
export default {
    name: 'bbody',
    props:['list','output'],
    components: {
        InputBar,
        ListContainer
    },
    methods:{
        add_item:function(item){
            this.list.push({key:false,value:item});
            this.output.push({key:false,value:item});
        }
    }
}
</script>
