<template>
<div class="container">
  <p>FOOTER1</p>
  <p>FOOTER2</p>
  <p>FOOTER3</p>
</div>
</template>

<script>
export default {
  name: 'MainFooter',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container
{
    background: red;
    display: flex;
    justify-content: space-around;
}
</style>
