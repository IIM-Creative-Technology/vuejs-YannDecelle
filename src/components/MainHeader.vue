<template>
<div class="container">
  <div>
    <p>LOGO</p>
    <p>TITLE</p>
  </div>
  <div>
    <a href="">Éditer</a>
    <a href="">Blog</a>
    <a href="">Connexion</a>
    <img src="../assets/sun.svg" alt="darkmode">
  </div>
</div>
</template>

<script>
export default {
  name: 'MainHeader',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container
{
  background: grey;
  display: flex;
  justify-content: space-between;
  align-items: center;

  div
    {
      display: flex;
    }
  div:first-child
    {
      justify-content: space-around;
      width: 10%;
    }
  div:last-child
    {
      justify-content: space-around;
      width: 75%;
    }
}
</style>
