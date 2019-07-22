<template>
  <div id="input_bar">
    <input type="text" v-model="item" class="input-text" v-on:keyup.enter="$emit('add_item',item);item=''">
    <button v-on:click="$emit('add_item',item);item=''">add</button>
  </div>
</template>

<script>
export default {
  name: 'input_bar',
  data:()=>{
    return{
      item : ""
    }
  }
}
</script>

