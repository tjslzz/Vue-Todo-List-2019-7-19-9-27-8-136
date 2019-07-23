<template>
<div id="bbody">
    <InputBar :list="list" />
    <ListContainer :output="list" :model="model"/>
</div>
</template>

<script>
import InputBar from './input_bar.vue';
import ListContainer from './list_container.vue';
export default {
    name: 'bbody',
    data() {
        return {
            list: []
        }
    },
    props: {
        model: {
            type: Function
        }
    },
    components: {
        InputBar,
        ListContainer
    }
}
</script>
