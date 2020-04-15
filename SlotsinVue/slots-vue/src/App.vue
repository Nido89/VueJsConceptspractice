<template>
  <div id="app">
   <Button>
     <template #icon>
               <i class="fas fa-shopping-cart"></i>
     </template>
      
      <span @click="test" class="text orange">
        {{ label }}
      </span>
   </Button>
 
  </div>
</template>

<script>

import Button from "./components/Button";
export default {
  data: () => {
    return {
      label:'Order Now'
    }
  },
  components: {
    Button
  },
  methods: {
    test(){
      console.log('Hello World');
    }
  },
};
</script>

<style lang="scss">
@import url("https://use.fontawesome.com/releases/v5.9.0/css/all.css");
body {
  display:flex;
  justify-content:center;
  align-items:flex-start;
  width:100%;
  height:100vh;
  padding:0;
  margin:0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 1rem;
}
#app{
  padding:20px;
  color:cadetblue;
  background-color:white
}
.orange{
  color:white;
  background-color:goldenrod;
}
</style>
