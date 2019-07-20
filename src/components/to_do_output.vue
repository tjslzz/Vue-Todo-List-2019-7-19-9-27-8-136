<template>
<div id="to_do_output">
    <ol>
        <Item v-for="(item) in list" v-bind:key="item.key" v-bind:item="item"/>
    </ol>
</div>
</template>

<script>
import Item from "./to_do_item.vue";
export default {
    name: 'to_do_output',
    props: ["list"],
    components:{Item}
}
</script>
