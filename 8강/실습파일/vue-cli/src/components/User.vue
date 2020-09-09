<template>
    <div class="component">
        <h1>The User Component</h1>
        <p>I'm an awesome User!</p>
        <button @click='changeName'>Change my Name</button>
        <p>parent data_name value = {{ name }}</p>    
        <p>Parent Age is {{age}}</p> 
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <app-user-detail 
                    :myName='name' 
                    @nameWasReset="name=$event"
                    :resetFn="resetName"
                    :userAge="age"
                ></app-user-detail>
            </div>
            <div class="col-xs-12 col-sm-6">
                <app-user-edit :userAge="age" @ageWasEdited="showEvent('35',$event)"></app-user-edit>
            </div>
        </div>
    </div>
</template>

<script>
    import UserDetail from './UserDetail.vue';
    import UserEdit from './UserEdit.vue';

    export default {
        data:function(){
            return{
                name:'Max',
                age:27
            };
        },methods:{
            changeName : function(){
                this.name='Anna';
            },
            resetName: function(){
                this.name ='Max'
            },
            showEvent : function(data,event){
                console.log("data====",event)
                console.log("data====",data);
                //this.age=data;

            }
        },
        components: {
            appUserDetail: UserDetail,
            appUserEdit: UserEdit
        }
    }
</script>

<style scoped>
    div {
        background-color: lightblue;
    }
</style>
