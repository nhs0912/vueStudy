<template>
    <div class="component">
         <h1>UserEdit.vue</h1>
        <h3>You may edit the User here</h3>
        <p>Edit me!</p>
        <p>User Age : {{userAge}}</p>
        <button @click="editAge(30)">Edit Age</button>
    </div>
</template>

<script>
import { eventBus } from '../main';

export default{
    props:['userAge'],
    methods:{
        editAge: function(userAge){
            // this.userAge = 30;
            this.$emit('ageWasEdited',userAge);
            // eventBus.$emit('ageWasEdited',this.userAge);
            //eventBus.changeAge(this.userAge);
        }
    }
}
</script>

<style scoped>
    div {
        background-color: lightgreen;
    }
</style>
