<template>
<li v-if="isBool">
       {{count}} <button @click="del">删除</button>
</li>
</template>
<script>
export default {
 props:["count","index"],
  data () {
    return {
     isBool:true
    }
  },
  methods:{
    del:function () {
     this.isBool=false
    }
  }
}
</script>