<template>
   <div>
                <h1>Filters & Mixins</h1>
                <p>{{text | to-lowercase}}</p>
                <hr>
                <input v-model="filterText">
                <ul>
                    <li v-for="(fruit,index) in filteredFruits" :key='index' >{{fruit}}({{index}})</li>


                </ul>
                <hr>
        </div>       
  
</template>

<script>

    import { fruitMixin } from './fruitMixin'
    export default {
        mixins: [fruitMixin],
        created(){
            console.log('Inside List Created Hook');
        }
    }
</script>

<style>

</style>
