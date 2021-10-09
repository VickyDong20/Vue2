<template>
<div>
    <h1>{{msg}}</h1>
    <button @click="sendData">passing data</button>
    </div>
</template>
<script>
export default{
     props:['msg'],
     data(){
         return{
             helloData:'i am child'
         }
     },
     
    methods:{
        sendData(){
            this.$emit('myevent',this.helloData)
        }
    }
  
}
</script>

<style scoped>


</style>
