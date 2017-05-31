<template>
  <div class="col-xs-3">
    <h2>NPCs</h2>
    <fighter v-for="fighter in fighters" v-bind:fighter="fighter" v-show="!fighter.isPC"></fighter>
  </div>
</template>
<script>
  import Fighter from './Fighter';

  export default {
    props: ['fighters'],
    components: {
      Fighter
    }
  }
</script>
<style>

</style>
