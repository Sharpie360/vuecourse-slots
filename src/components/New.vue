<template>
  <div>
    <h3>New Quote</h3>
    <button @click="counter++">Plus One</button>
    {{ counter }}
  </div>
</template>

<script>
  export default {
    data () {
      return {
        counter: 0
      }
    },
    destroyed () {
      console.log('component destroyed')
    },
    deactivated() {
      console.log('component deactivated')
    },
    activated() {
      console.log('component activated')
    },
  }
</script>

<style>

</style>

