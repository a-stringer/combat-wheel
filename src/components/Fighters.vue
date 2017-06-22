<template>
  <div class="row">
    <div class="col-xs-2">
      <h2>PCs</h2>
      <fighter v-for="fighter in fighters" v-bind:fighter="fighter" v-if="fighter.isPC&&!fighter.inCombat" v-on:join-combat="joinCombat"></fighter>
    </div>
    <div class="col-xs-2">
      <h2>NPCs</h2>
      <fighter v-for="fighter in fighters" v-bind:fighter="fighter" v-if="!fighter.isPC&&!fighter.inCombat" v-on:join-combat="joinCombat"></fighter>
    </div>
    <div class="col-xs-2">
      <h2>Stuff</h2>
      <fighter v-for="fighter in fighters" v-bind:fighter="fighter" v-if="fighter.inCombat" v-on:leave-combat="leaveCombat"></fighter>
    </div>
  </div>
</template>
<script>
  import Fighter from './Fighter';

  export default {
    props: ['fighters'],
    components: {
      Fighter
    },
    methods: {
      joinCombat (fighter) {
        const fighterIndex = this.fighters.indexOf(fighter);
        this.fighters[fighterIndex].inCombat = true;
      },
      leaveCombat (fighter) {
        const fighterIndex = this.fighters.indexOf(fighter);
        this.fighters[fighterIndex].inCombat = false;
      }
    }
  }
</script>
<style>

</style>
