<template>
<ul id="to_do_option">
    <li><a href="#" v-on:click="$emit('all')">ALL</a></li>
    <li><a href="#" v-on:click="$emit('active')">Active</a></li>
    <li><a href="#" v-on:click="$emit('complete')">Complete</a></li>
</ul>
</template>

<script>
export default {
    name: 'to_do_option'
}
</script>
