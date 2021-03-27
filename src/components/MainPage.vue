<template>
<div class="container">
  <h1>Articles</h1>
  <input type="text" id="title" placeholder="Titre"><input type="text" id="content" placeholder="Contenu"><button v-on:click="addBlog(title)">Ajouter un article</button>
  <div class="blogCard" v-for="title in titles" :key="title.index">
    <div class="blogInfo">
      <h2 class="blogTitle">{{title.title}}</h2>
      <p class="blogContent">{{title.content}}</p>
    </div>
        <button type="submit">Éditer</button>
        <button type="submit" v-on:click="removeBlog(title)">X</button>
  </div>
</div>
</template>

<script>
import Vue from 'vue';
import Vuex from 'vuex';

Vue.use(Vuex);

new Vuex.Store
(
  {
    state:{},
    mutations:{},
    methods:{}
  }
)

export default {
  name: 'MainPage',
  props: {
    msg: String
  },
 methods:{
    removeBlog: function(titles)
    {
      let currentID = this.titles.indexOf(titles);
      var debugID = currentID +1;
      this.titles.splice(currentID, 1);
      console.log('Ligne numéro '+debugID+' a été supprimée.');
      console.log(debugID);
    },
    addBlog: function(titles)
    {
      let currentID = this.titles.indexOf(titles);
      var titleInput = document.getElementById('title').value;
      var contentInput = document.getElementById('content').value;
      this.titles.push({title: titleInput, content: contentInput});
      console.log(currentID);
      titleInput.value = '';
      contentInput.value ='';
    }     
  },
    data: function()
    {
      return {titles: [{title: "Hello", content: "Description, de l'article"}]
      };
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container
{
    flex-grow:1;
}
</style>
