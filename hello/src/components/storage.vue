<template>
    <table>
        <thead>
            <th>name</th>
            <th>number</th>
        </thead>
        <tr v-for="(fruit,index) of fruits" :key="index">
            <td>{{fruit.name}}</td>
            <td>{{fruit.number}}</td>
        </tr>
    </table>
</template>

<script>
export default{
    data(){
        return{
            fruits:[{name:'strawberry',number:50},
            {name:'cherry',number:20},
             {name:'banana',number:60},
            ]
        }
    }
}
</script>

<style scoped>

</style>
