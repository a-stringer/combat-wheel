<template>
  <div>
    <h3>{{fighter.name}}</h3>
    <h4>Initiative: {{fighter.joinBattle}}</h4>
  </div>
</template>

<script>
  export default {
    props: ['fighter'],
    data () {
      return {
        isEditing: false
      }
    }
  }
</script>

<style>

</style>
