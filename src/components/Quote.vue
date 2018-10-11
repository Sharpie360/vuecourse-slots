<template>
  <div class="outer">
    <div class="title">
      <slot name="title"></slot>
    </div>
    <hr>
    <div class="content">
      <slot name="content"></slot>  
    </div>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  .outer {
    border: 1rem solid #212121
  }

</style>
