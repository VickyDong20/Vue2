<template>
<div>
    <button @click="minus">-</button>
    <span>{{qu}}</span>
    <button @click="plus">+</button>
    </div>
</template>

<script>


export default {
    props:['qu','i'],
    data(){
        return{}
    },
    methods:{
        minus(){
            this.$emit('minus',this.i)
        },
         plus(){
            this.$emit('plus',this.i)
        }
    }
   
}
</script>
