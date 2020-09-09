<template>
    <div class="component">
        <h1>UserDetail.vue</h1>
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User Name: {{ switchName() }}</p>
        <p>User Age: {{ userAge }}</p>
        <button @click="resetName('Max')">Reset Name</button>
        <button @click="resetFn()">Reset Name</button>
    </div>
</template>

<script>
import { eventBus } from '../main';
export default{
    props : {
        myName: {
            type : String
            // required: true,
            // default : 'Max'
        },
        resetFn: Function,
        userAge: Number
 
    },
    methods:{
        switchName:function(){
            return this.myName.split("").reverse().join("");
        },
        resetName:function(data){
            //this.myName='Max'; 
            this.$emit('nameWasReset',data);
           
        }
    }
    // ,created: function(){
    //     eventBus.$on('ageWasEdited',(age) =>{
    //         this.userAge = age;
    //     });
    // }
}
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
