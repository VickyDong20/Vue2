<template>
<div>
  
  <ul v-for="(fruit,index) of fruits" :key='index'>
    <li>{{fruit.name}} price:{{fruit.prize}}
     <counter :qu='fruit.qu' :i='index' @minus='minus' @plus="plus">   </counter>
    </li>
  </ul>

</div>
</template>
<script>
import counter from './counter.vue'
export default{
    components:{counter},
  data(){
    return{
      fruits:[{name:'banana',prize:4.6,qu:0},
      {name:'apple',prize:3,qu:0},
      {name:'watermelon',prize:5,qu:0},],


    }
  },
   methods:{
      minus(i){
          if(this.fruits[i].qu>0)
          {this.fruits[i].qu--}
      },
      plus(i){
          this.fruits[i].qu++
      }

    }

}

</script>

<style>

</style>
