<template>
    <div>
        <!-- <p>Counter is : {{ counter }}</p> -->
        <p>Counter is : {{ doubleCounter }}</p>
        <!-- <p> Number of Clicks : {{clicks}}</p> -->
        <p> Number of Clicks : {{stringCounter}}</p>
    </div>
</template>

<script>
    import {mapGetters} from 'vuex';
    export default {

        coumputed : mapGetters([
            'doubleCounter',
            'stringCounter'
        ])
    // computed:{
    //     counter(){
    //         return this.$store.getters.doubleCounter;
    //         // return this.$store.state.counter * 2;
    //     },
    //     clicks(){
    //         return this.$store.getters.stringCounter;
    //     }
    // }
    }
</script>

<style>

</style>