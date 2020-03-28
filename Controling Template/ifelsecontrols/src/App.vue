<template>
<div id="app">
  <button @click="showText=!showText">ClickMe to Hide</button>
  <div class="textbox" v-if="showText">
    <br><b>Incubation Period</b><br>
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
<div class="textbox" v-else-if>
  <br><b>symptoms</b><br>
  If you develop emergency warning 
  signs for COVID-19 get medical
   attention immediately. 
   Emergency warning signs include*:

    Trouble breathing
    Persistent pain or pressure in the chest
    New confusion or inability to arouse
    Bluish lips or face
    *This list is not all inclusive. 
    Please consult your medical provider for
    any other symptoms that are severe or concerning.
</div>
<div class="textbox" v-show="showText">
  <br><b>Mortality Rate</b><br>
  3.4% Mortality Rate estimate by the World Health Organization (WHO) as of March 3
  In his opening remarks at the March 3 media briefing on Covid-19, WHO Director-General Dr Tedros Adhanom Ghebreyesus stated:

  “Globally, about 3.4% of reported COVID-19 cases have died. By comparison, seasonal flu generally kills far fewer than 1% of those infected.” [13]

  Initial estimate was 2%
  Initially, the World Health Organization (WHO) had mentioned 2% as a mortality rate estimate in a press conference on Wednesday, January 29 [1][2] and again on February 10. However, on January 29 WHO specified that this was a very early and provisional estimate that might have changed. Surveillance was increasing, within China but also globally, but at the time it was said that:

  We don't know how many were infected ("When you look at how many people have died, you need to look at how many people where infected, and right now we don't know that number. So it is early to put a percentage on that."[1][2]).
  The only number currently known is how many people have died out of those who have been reported to the WHO.
  It is therefore very early to make any conclusive statements about what the overall mortality rate will be for the novel coronavirus, according to the World Health Organization [1][2].
</div>
</div>
</template>

<script>
  export default {
    data:()=> {
      return{
        showText : true
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
    display:flex;
    justify-content: center-start;
    align-items: center;
    flex-direction:column;
    padding: 30px;
    width:calc(100% -20px);
    height: 100%;
    color: rgb(0, 183, 255);
   

  }
  button{
    font-size: 1.2rem;
    margin-bottom: 10px;
    border:none;
    padding: 5px 10px;
    color: rgb(205, 79, 255);
    background-color: rgb(0, 225, 255);
    align-items: center;
  }
  .textbox{
    padding: 20px;
    width:calc(100% - 40px);
    max-width: 480px;
    border: 1px solid #cccccc;
    font-size: 1.2rem;
    color: rgb(73, 73, 73);
    background-color: azure;
    &.dark{
      color: #efefef;
      background-color: rgb(39, 39, 39);
    }
  }

</style>
