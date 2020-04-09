<template>
  <div id="app">
    <div class="title">MyTitle</div>
    <Status />
     <Status />
      <Status />
       <Status />
  </div>
</template>

<script>
import Status from './components/Status.vue'

export default {
 components: {
   Status
 }
}
</script>

<style>
  *{
    font-size: 1.6rem;
  }

  .title{
    color:red;

    }


</style>
