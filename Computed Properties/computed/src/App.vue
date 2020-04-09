<template>
  <div id="app">
    <button @click="status= !status">Change status</button>
  {{ firstname }} {{ lastname }}  
  <br>
  {{ getName() }}  
  <br>
  <br>
  {{ name }}  
  <br>
  {{ status }}
  <ul>
    <li v-for="movie in unwatchedMovies" :key="movie.title">{{movie.title}}</li>
  </ul>
  </div>
</template>

<script>


export default {
data:() => {
  return{
    firstname:'Nido',
    lastname: 'Jalal',
    status:false,
    movies:[
      {title:'Spiderman',watched:true},
      {title:'Hulk',watched:false},
      {title:'Avengers',watched:false},
      {title:'CaptainMarvel',watched:false}
      ]
  }
},
computed: {
  name(){
      console.log('computed');
    return this.firstname +' ' +this.lastname;
  },
  unwatchedMovies(){
    return this.movies.filter(movie => movie.watched===false);
  }
},

methods: {
  getName(){
    console.log('method');
    return this.firstname +' ' +this.lastname;
  }
},
}
</script>
<style lang="scss">
  #app {
    display:flex;
    justify-content: center-start;
    align-items: center;
    flex-direction:column;
    padding: 30px;
    width:calc(100% -20px);
    height: 100%;
    color: rgb(238, 255, 0);
  }
    body{
    margin:0;
    padding: 0;
    font-family: sans-serif;
    font-size: 1rem;
    background-color: rgb(71, 71, 71);
  }
</style>>
