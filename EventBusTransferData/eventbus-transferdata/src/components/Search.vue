<template>
  <div id="search">
      <input type="text" v-model="value">
      <i class="fas fa-search" @click="emitSearchValue"></i>
  </div>
</template>

<script>
import { EventBus } from '@/event-bus.js'
export default {
    data:() => {
        return {
            value:""
        };
    },
    methods: {
        emitSearchValue(){
            EventBus.$emit('search-value',this.value);
        }
    }
};
</script>

<style lang="scss" scoped>
#search{
color: rgb(255, 255, 255);
.fa, .far, .fas {
    background-color: green;
}
}
.fas fa-search{
    color: chartreuse;
}
input{
    color: rgb(0, 97, 97);
    border-color: blueviolet;
}
</style>