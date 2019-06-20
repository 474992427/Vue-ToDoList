<template>
<div>
    <h2>待做的事</h2>
    <input type="text" v-model="thing">
    <button @click="add">添加</button>
</div>
</template>
<script>
import bus from'../assets/eventBus'

export default {

  data () {
    return {
     thing:'',
    }
  },
  methods:{
    add:function(){
      bus.$emit("customEvent",this.thing)
      this.thing="";
      //console.log(this.thing);
  }
  }
  
}
</script>