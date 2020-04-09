<template>
  <div id="app" :style="{backgroundColor: status ?'#333' : '#fff'}">
    <button @click="status=!status">Change Status</button>
  </div>
</template>

<script>


export default {
  data: () =>{
    return {
      status:false
    }
  },
  watch: {
    status(newStatus,oldStatus){
      console.log('The status has changed! From'+ oldStatus +'to'+ newStatus);
    localStorage.setItem("status",newStatus);
    }

  },
  created() {
    this.status=JSON.parse(localStorage.getItem("status"));
  },
}
</script>

<style lange="scss">

#app{

   font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
 
}
</style>
