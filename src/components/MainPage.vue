<template>
<div class="container">
  BODY
</div>
</template>

<script>
export default {
  name: 'MainPage',
  props: {
    msg: String
  },
      methods:
  {
    addElement: function ()
    {
        console.log('Element created');
    },
    removeElement: function (index)
    {
        this.tasks.splice(index, 1);
        console.log('Element deleted');
        this.tasks.push();
    },
  },
    data() {
    return {
      tasks: [
        {id: 1, task: 'Premier'},
        {id: 2, task: 'Premier'},
        {id: 3, task: 'Premier'},
        {id: 4, task: 'Premier'},
        {id: 5, task: 'Premier'},
        {id: 6, task: 'Premier'},
      ]
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container
{
    background: lime;
    flex-grow:1;
}
</style>
