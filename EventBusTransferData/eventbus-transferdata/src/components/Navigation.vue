<template>
   <div id="navigation">
       <Menu />
       <Search />
   </div>
</template>
<script>
import Menu from "./Menu.vue";
import Search from "./Search.vue";



export default {
    components: {
        Menu,
        Search
    }
    
};
</script>