<template> <!-- use for ArticleConponent and GreetFirst component -->
  <div>
    Hello {{ name }}, You are viewing {{ name }}, Here is a example of Component, Component Props, Prop Types and Validations
  </div>
  <!--<h5>Text size increse on button click</h5>
   <div :style="{ fontSize: postFontSize + 'px' }">
    <GreetFirst name="Batman" movie="Batman Forever" />
    <GreetFirst name="Superman" movie="Superman Returns" />
    <GreetFirst name="Spiderman" movie="Spider-Man: No Way Home" />
    <GreetFirst :name="name" movie="movieName" @enlarge-text="postFontSize += 0.1" /> //dynamic component value  
  </div> -->
  <ArticleComponent id="movies" title="Article Title" :likes="50" :isPublished="true"></ArticleComponent>


  <hr/>

</template>

<script>
// import GreetFirst from './components/GreetFirst.vue'
import ArticleComponent from './components/ArticleComponent.vue'

export default {
  name: 'App',
  components: {
    // GreetFirst,
    ArticleComponent,
  },
  data() {
    return {
      name: 'Ironman',
      movieName: 'Ironman 3',
      postFontSize: 15
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

hr {
  border: 2px solid #035891;
}
</style>
