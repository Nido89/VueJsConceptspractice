<template>
<div id="app">
  <button :style="{backgroundColor: darkMode? '#813931': 'aquamarine'}" @click="darkMode=!darkMode">ClickMe to DarkMode</button>
  <div class="textbox" :class="{'dark':darkMode}">
    2-14 days represents the current 
    official estimated range
     for the novel coronavirus COVID-19.
However, a case with an incubation period 
of 27 days has been reported by Hubei 
Province local government on Feb. 22 [12]
In addition, a case with an incubation
 period of 19 days
 was observed in a JAMA study of 5 cases 
 published on Feb. 21. [13]
An outlier of a 24 days incubation 
period had been for the 
first time observed in a Feb. 9 study.
[11] WHO said at the time that this 
could actually
 reflect a second exposure rather than a 
 long incubation period,
 and that it wasn't going to change 
 its recommendations.
  </div>
</div>
</template>

<script>
  export default {
    data:()=> {
      return{
        darkMode: false
        }
      
    }
      
  }
</script>

<style <style lang="scss">
  

  body{
    margin:0;
    padding: 0;
    font-family: sans-serif;
    font-size: 1rem;
  }
  

  #app {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: column;
    padding: 10px;
    width:calc(100% -20px);
    height: calc(100vh -20px);
    color: chartreuse;
    background-color: cadetblue;

  }
  button{
    font-size: 1.2rem;
    margin-bottom: 10px;
    border:none;
    padding: 5px 10px;
    color: cadetblue;
    background-color: aquamarine;
    align-items: center;
  }
  .textbox{
    padding: 20px;
    width:calc(100% - 40px);
    max-width: 480px;
    border: 1px solid #cccccc;
    font-size: 1.2rem;
    color: crimson;
    background-color: azure;
    &.dark{
      color: #efefef;
      background-color: rgb(39, 39, 39);
    }
  }

</style>
