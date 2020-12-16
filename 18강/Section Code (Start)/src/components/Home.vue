<template>
  <div>
    <h1>Trade or View your POrtfolio</h1>
    <h6>You may Sve & Load your Data</h6>
    <h6>Click on 'End Day' to begin a New Day!</h6>
    <hr>
    <P>Your Funds: {{funds | currency}} </P>


  </div>
</template>

<script>
export default {
    computed: {
      funds() {
         return this.$store.getters.funds;
      }
    }

}
</script>

<style>

</style>