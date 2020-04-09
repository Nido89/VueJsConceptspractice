<template>
  <div id="app">
    <Navigation />
    <Article />
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Article from './components/Article.vue'

export default {
  name: 'App',
  components: {
   Navigation,
   Article
}
};
</script>

<style lang="scss">

@import url("https://use.fontawesome.com/releases/v5.13.0/css/all.css");

body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin:0;
  padding:0;
  font: size 1rem;
}

</style>