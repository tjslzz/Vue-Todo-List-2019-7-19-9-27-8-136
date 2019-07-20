<template>
  <div id="to_do_input">
    <input type="text" v-model="item">
    <button v-on:click="$emit('add_item',item)">add</button>
  </div>
</template>

<script>
export default {
  name: 'to_do_input',
  data:()=>{
    return{
      item : ""
    }
  }
}
</script>

