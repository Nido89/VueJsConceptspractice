<template>
    <div id="article">
        <i class="fas fa-newspaper"></i>
        <div class="teaser"
        v-for="(item, index) in filteredTeaser"
        :key="index">
        <b>{{ item.title }} </b>
        <p>{{ item.text }} </p>
        </div>
    </div>
</template>

<script>
import { EventBus } from '@/event-bus.js'

export default {
    data: () => {
        return {
            searchvalue: '',
            teaser: [
                {
                    title:"Transfer Data Between Components in Vue JS",
                    text:"How you can transfer data between components in vue js? It is because of the communication between the parents component and child component."
                },
                {
                    title:"Using components in Vue Js and how to register them",
                    text:"How you can transfer data between components in vue js? It is because of the communication between the parents component and child component."
                },
                {
                    title:"Transfer Data Between Components in Vue JS",
                    text:"How you can transfer data between components in vue js? It is because of the communication between the parents component and child component."
                },
                {
                    title:"Transfer Data Between Components in Vue JS",
                    text:"How you can transfer data between components in vue js? It is because of the communication between the parents component and child component."
                },
                {
                    title:"Transfer Data Between Components in Vue JS",
                    text:"How you can transfer data between components in vue js? It is because of the communication between the parents component and child component."
                }
            ]
        };
    },
    computed: {
        filteredTeaser(){
            return this.teaser.filter(item => 
            item.title.toLowerCase().includes(
                this.searchvalue.toLowerCase()
            )
            );
        }
    },
    created (){
        EventBus.$on('search-value', (value) =>{
            this.searchvalue = value;
        });
    }
};
</script>

<style lang="scss" scoped>
#article{
    width:100%;
    display: block;
    border-block: black;
    background: rgb(167, 167, 255);
    .teaser {
        background-color: rgb(212, 0, 0);
        color: white;
    }

}

</style>