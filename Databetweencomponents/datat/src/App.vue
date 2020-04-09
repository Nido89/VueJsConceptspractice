<template>
  <div id="app">
    <List :listdata="items" @clickedItem="getClickedItem"/>
    {{ clickedItem }}
  </div>
</template>

<script>
import List from './components/List.vue'

export default {
  data:() => {
    return{
      items: ['first','second','third','fourth','fifth'],
      clickedItem:''
    }
  },
  components:{
    List
  },
  methods: {
    getClickedItem(value) {
      this.clickedItem=value;

    }
  },
}
</script>

<style>
*{
  background:rgb(0, 94, 117);

 
}
#app{
  
  color: white;
  justify-content:center ;

  
  
}
</style>