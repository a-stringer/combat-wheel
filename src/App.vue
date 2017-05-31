<template>
  <div id="app" class="container">
    <div class="row">
      <party-list v-bind:fighters="fighters"></party-list>
      <npc-list v-bind:fighters="fighters"></npc-list>
    </div>

  </div>
</template>

<script>
import PartyList from './components/PartyList';
import NpcList from './components/NpcList';

export default {
  name: 'app',
  components: {
    PartyList,
    NpcList
  },
  data () {
    return {
      fighters: [{
        name: 'Park',
        joinBattle: 1,
        isPC: true,
        inCombat: false,
        dvMod: 0,
        key: 0
      },
      {
        name: 'Sabine',
        joinBattle: 2,
        isPC: true,
        inCombat: false,
        dvMod: 0,
        key: 1
      },
      {
        name: 'Cole',
        joinBattle: 3,
        isPC: true,
        inCombat: false,
        dvMod: 0,
        key: 2
      },
      {
        name: 'Guy',
        joinBattle: 4,
        isPC: true,
        inCombat: false,
        dvMod: 0,
        key: 3
      },
      {
        name: 'Rune',
        joinBattle: 5,
        isPC: true,
        inCombat: false,
        dvMod: 0,
        key: 4
      },
      {
        name: 'Mook',
        joinBattle: 1,
        isPC: false,
        inCombat: false,
        dvMod: 0,
        key: 5
      }]
    }
  }
}
</script>

<style>

</style>
