<template>
  <div>
    <h3>{{fighter.name}}</h3>
    <h4>Initiative: {{fighter.joinBattle}}</h4>
    <button class="btn" v-show="!fighter.inCombat" v-on:click="joinCombat(fighter)">Join Battle</button>
    <button class="btn" v-show="fighter.inCombat" v-on:click="leaveCombat(fighter)">Leave Battle</button>
  </div>
</template>

<script>
  export default {
    props: ['fighter'],
    methods:{
      joinCombat(fighter){
        this.$emit('join-combat', fighter);
      },
      leaveCombat(fighter){
        this.$emit('leave-combat', fighter);
      }
    }
  }
</script>

<style>

</style>
