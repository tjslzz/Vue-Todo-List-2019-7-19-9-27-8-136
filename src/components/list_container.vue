<template>
<div id="to_do_list">
    <ol>
        <Item v-for="(item) in list" v-bind:key="item.key" v-bind:item="item"/>
    </ol>
</div>
</template>

<script>
import Item from "./list_item.vue";
export default {
    name: 'to_do_list',
    props: ["list"],
    components:{Item}
}
</script>
