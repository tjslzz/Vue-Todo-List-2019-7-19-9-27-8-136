<template>
  <div id="input_bar">
    <input type="text" v-model="item" class="input-text" @keyup.enter="add_item(item)">
    <button @click="add_item(item)">add</button>
  </div>
</template>

<script>
let id = 0;
let get_id=()=>{
  return id++;
}
export default {
  name: 'input_bar',
  data(){
    return{
      item : ""
    }
  },
  props:['list'],
  methods:{
    add_item(item){
      this.list.push({id:get_id(),checked:false,value:item});
      item='';
    }
  }
}
</script>

