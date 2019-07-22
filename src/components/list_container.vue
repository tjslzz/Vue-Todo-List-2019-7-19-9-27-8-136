<template>
<div id="to_do_list">
    <ol>
        <Item v-for="(item) in list" :key="item.id" :item="item" />
    </ol>
</div>
</template>

<script>
import Item from "./list_item.vue";
export default {
    name: 'to_do_list',
    data() {
        return {
            list: []
        }
    },
    props: {
        output: {
            type: Array,
            default: () => []
        },
        model: {
            type: String,
            default: () => "all"
        }
    },
    components: {
        Item
    },
    mounted() {
        this.list = this.output;
    },
    watch: {
        model() {
            switch(this.model){
                case "all" : this.list = this.output;break;
                case "active" : this.list = this.output.filter(i => !i.checked);break;
                case "complete" : this.list = this.output.filter(i => i.checked);break;
            }
        }
    }
}
</script>
