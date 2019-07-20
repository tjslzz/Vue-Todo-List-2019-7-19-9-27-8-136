<template>
<div id="to_do_output">
    <br>
    <ol>
        <li v-for="item in list" v-bind:key="item.key">
          <input type="checkbox">
          {{ item }}
        </li>
    </ol>
</div>
</template>

<script>
export default {
    name: 'to_do_output',
    props: ["list"]
}
</script>
