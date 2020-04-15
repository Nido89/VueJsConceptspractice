<template>
  <button>
        <span class="icon orange">
           <slot name="icon"> </slot>
      </span>
   
     <slot>
          <span class="text orange">
              Submit
          </span>
    
     </slot>
  </button>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>

</style>