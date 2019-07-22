<template>
<div id="to_do_list">
    <ol>
        <Item v-for="(item) in output" :key="item.id" :item="item" />
    </ol>
</div>
</template>

<script>
import Item from "./list_item.vue";
export default {
    name: 'to_do_list',
    data() {
        return {
            output: []
        }
    },
    props: ["list", "model"],
    components: {
        Item
    },
    mounted() {
        if (this.model == "all") {
            this.output = this.list;
        } else if (this.model == "active") {
            this.output = this.list.filter(i => !i.checked);
        } else if (this.model == "compelete") {
            this.output = this.list.filter(i => i.checked);
        }
    }
}
</script>
