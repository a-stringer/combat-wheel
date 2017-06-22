<template>
  <div>
    <div v-show="!isEditing">
      <h3>{{fighter.name}}</h3>
      <h4>Initiative: {{fighter.joinBattle}}</h4>
      <button class="btn btn-warning" v-on:click="showForm">Edit</button>
      <button class="btn btn-danger" v-show="!fighter.inCombat" v-on:click="joinCombat(fighter)">Join Battle</button>
      <button class="btn btn-success" v-show="fighter.inCombat" v-on:click="leaveCombat(fighter)">Leave Battle</button>
    </div>
    <div class="form-group" v-show="isEditing">
      <label for="name">Fighter Name</label>
      <input id="name" class="form-control" type='text' v-model="fighter.name">
      <label for="joinbattle">Join Battle Results</label>
      <input id="joinbattle" class="form-control" type='number' v-model="fighter.joinBattle">
      <button class="btn btn-warning" v-on:click="hideForm">Done Editing</button>
    </div>
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
      },
      showForm () {
        this.isEditing = true
      },
      hideForm () {
        this.isEditing = false
      }
    },
    data () {
      return {
        isEditing: false
      }
    },
  }
</script>

<style>

</style>
