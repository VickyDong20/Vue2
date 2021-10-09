<template>
<div>
  <h1>{{helloData}}</h1>
    <hello @myevent='changedata' :msg="message"></hello>
 
  <storage></storage>

 
<!-- <h1 v-show="isLoginin">{{message}}</h1>

<ul>
  <li v-for="(fruit,index) of fruits" :key="index">
    <p>fruit name:{{fruit}}</p>
    <p>number:{{index}}</p>
  </li>
</ul>
<table>
  <thead>
  <th>name</th>
  <th>gender</th></thead>
  <tbody>
  <tr v-for="(student,index) of students" :key="index">
    <td>{{student.name}}</td>
    <td>{{student.gender}}</td>
  </tr>
  </tbody>
</table> -->
</div>
</template>

<script>
import hello from "./components/hello.vue";
import storage from './components/storage.vue';

export default{
  components: { hello, storage },
  data(){
    return{
message:'Welcom to our fruits shop',
     // isLoginin:'true',
     // fruits:['strawberry','blueberry','cherry','banana'],
        //students:[{name:'li',gender:'female'},{name:'jack',gender:'male'}],
  helloData:'',

  
  }},
  methods:{
    changedata(helloData){
this.helloData=helloData
    }
  }
}
</script>

<style>

</style>
