<template>
    <div>
    <h3> New </h3>
    <button @click="counter++">Increase!</button>
    <p>{{ counter }}</p>
    </div>    
</template>

<script>
    export default{
       data:function(){
           return {
               counter:0
           };
       },
       destroyed : function(){
           console.log('Destroyed!');
       },
       deactivated(){
           console.log('Deactivated');
       },
       activated(){
           console.log("activated")
       }
    }
</script>

<style >

</style>
