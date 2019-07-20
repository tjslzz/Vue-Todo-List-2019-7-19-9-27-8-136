<template>
<li id="to_do_item" v-bind:class="{checked:item.key}">
    <input type="checkbox" v-model="item.key">
    {{ item.value }}
</li>
</template>

<script>
export default {
    name: 'to_do_item',
    props: {item:Object}
}
</script>
