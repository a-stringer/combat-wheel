<template>
  <div id="app" class="container">
    <fighters v-bind:fighters="fighters"></fighters>
  </div>
</template>

<script>
import Fighters from './components/Fighters';

export default {
  name: 'app',
  components: {
    Fighters
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
