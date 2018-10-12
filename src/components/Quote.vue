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
    border: 1rem solid #212121;
    background-color: #03A9AC;
    margin: 1rem 0;
    padding: 1rem;

    width: 100%;

    box-shadow: 0px 0px 25px rgba(247, 247, 247, .0);
    transition: box-shadow 0.1s;

    border-radius: .75rem;
  }
  .outer:hover {
    box-shadow: 0px 0px 25px rgba(247, 247, 247, .5);
  }
  .title {
    text-shadow: 1px 1px 5px rgba(22, 22, 22, 0.3)
  }
  .content {
    font-weight: 400;
    color: rgb(53, 53, 53);
  }

</style>
