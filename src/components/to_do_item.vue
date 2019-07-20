<template>
<li id="to_do_item" v-bind:class="{checked:item.key}">
    <input type="checkbox" v-on:click="choose()" v-bind="{checked:item.key}">
    {{ item.value }}
</li>
</template>

<script>
export default {
    name: 'to_do_item',
    props: {item:Object},
    methods: {
        choose() {
            if (this.item.key) {
                this.item.key = false;
            } else {
                this.item.key = true;
            }
        }
    }
}
</script>
