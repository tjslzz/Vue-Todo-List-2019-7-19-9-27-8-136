<template>
<li id="list_item" v-bind:class="{checked:item.key}">
    <input type="checkbox" v-model="item.key">
    <span @dblclick="editable" :contenteditable="edit" @input="updatable" ref="info">{{ item.value }}</span>
</li>
</template>

<script>
export default {
    name: 'list_item',
    props: {
        item: Object
    },
    data: () => {
        return {
            edit: false
        }
    },
    methods: {
        editable() {
            this.edit = true;
        },
        updatable() {
            this.item.value = this.$refs.info.innerHTML;
        }
    }
}
</script>
