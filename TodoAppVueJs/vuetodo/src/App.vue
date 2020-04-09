<template>
  <div id="app">
    <Header v-on:createTodo="createTodo" />
      <Todos v-bind:todos="todos" v-on:removeTodo="removeTodo"/>
   
  </div>
</template>

<script>
  import Header from './components/Header.vue';
  import Todos from './components/Todos';
  let todos = [
    {
      id:"1",
      name:"Write Vuejs Code",
      done:false
    },
    {
      id:"2",
      name:"Make a CRUD App",
      done:false
    },
    {
      id:"3",
      name:"Do backend with Django",
      done:false
    },
    {
      id:"4",
      name:"Do debugging",
      done:false
    },
    {
      id:"5",
      name:"Do workout",
      done:false
    }
  ];

export default {
  name: 'App',
  components: {
    Header,
    Todos
  },
  data: function(){
    return{
      todos:todos
    }
  },
  methods : {
    createTodo: function(todo){
     let todoObject= {
       id : Math.floor(Math.random()  *100000000),
       name: todo,
       done:false
     }
      this.todos.push(todoObject);
    },
    removeTodo: function(id){
      this.todos=this.todos.filter(todo => todo.id != id );
    }
  }
}
</script>

<style lang="scss">
  

body{
    margin:0;
    padding: 0;
    background-color: rgb(0, 198, 233);
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;

    
}
</style>
