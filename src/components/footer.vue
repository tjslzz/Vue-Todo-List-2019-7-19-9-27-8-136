<template>
<ul id="ffooter">
    <li><a href="#" v-on:click="$emit('all');model=1" v-bind:class="{ selected: model==1 }">ALL</a></li>
    <li><a href="#" v-on:click="$emit('active');model=2" v-bind:class="{ selected: model==2 }">Active</a></li>
    <li><a href="#" v-on:click="$emit('complete');model=3" v-bind:class="{ selected: model==3 }">Complete</a></li>
</ul>
</template>

<script>
export default {
    name: 'ffooter',
    data:()=>{
        return{
            model:0
        }
    }
}
</script>
