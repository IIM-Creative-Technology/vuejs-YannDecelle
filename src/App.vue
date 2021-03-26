<template>
  <div id="app">
    <MainHeader></MainHeader>
    <MainPage></MainPage>
    <MainFooter></MainFooter>
  </div>
</template>

<script>
import MainHeader from './components/MainHeader.vue';
import MainPage from './components/MainPage.vue';
import MainFooter from './components/MainFooter.vue';

export default {
  name: 'App',
  components: {
    MainHeader,
    MainPage,
    MainFooter,
  },
}
</script>

<style>
body
{
  margin: 0;
  padding: 0;
}

#app
{
  display: flex;
  flex-direction: column;
  min-height:100vh;
}
</style>
