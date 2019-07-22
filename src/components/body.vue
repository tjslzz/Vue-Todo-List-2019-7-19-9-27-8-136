<template>
<div id="bbody">
    <InputBar :list="list"/>
    <ListContainer :list="output" model="type"/>
</div>
</template>

<script>
import InputBar from './input_bar.vue';
import ListContainer from './list_container.vue';
export default {
    name: 'bbody',
    data(){
        return{
            list:[]
        }
    },
    props:{
        type:String
    },
    components: {
        InputBar,
        ListContainer
    }
}
</script>
