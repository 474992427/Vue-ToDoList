<template>
<div>
    <ul>
       <ToDoItem v-for="(tmp,index) in myMsg" :count="tmp" :key="index"></ToDoItem>
    </ul>
</div>
</template>
<script>
import ToDoItem from '@/components/ToDoItem'
import bus from'../assets/eventBus'
export default {
  data () {
    return {
     myMsg:[],
    }
  },
  mounted:function(){
      bus.$on("customEvent",msg=>{
          console.log(this.myMsg)
          this.myMsg.push(msg);
      })
  },
  components:{
      ToDoItem,
      
  }
}
</script>