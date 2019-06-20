<template>
<form @submit.prevent>
           <ToDoInput></ToDoInput>
           <ToDoList></ToDoList>
    </form>
</template>
<script>
import ToDoInput from '@/components/ToDoInput'
import ToDoList from '@/components/ToDoList'
export default {
  
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
      ToDoInput,
      ToDoList,
  }
}
</script>