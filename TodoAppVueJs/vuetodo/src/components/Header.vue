<template>
    <header>
        <input type="text" name="todoInput" v-model="todoValue" placeholder="What do you have to do today ?">
        <button class="submit" v-on:click="createTodo">CreateTask</button>
    </header>
</template>

<script>

export default {
    name: "Header",
    data: function() {
        return {
            todoValue: ""
        }
    },
    methods : {
        createTodo: function(){
            this.$emit('createTodo',this.todoValue);
            this.todoValue= "";
        }
    }
   
}
</script>

<style lang="scss" scoped>


header{
    display: flex;
    input {
        flex: 1;
        height:50px;
        box-sizing: border-box;
        font-size: 20px;
        text-indent: 25px;
    }
    .submit{
        width: 100px;
        height: 50px;
        font-size: 17px;
        line-height: 50px;
        cursor: pointer;
        background-color: lightgreen;
        border: none;
        outline: none;
        color: rgb(255, 17, 0);
        font-weight: 700;

        &:hover{
            background-color: darken($color: #00d4f0, $amount: 10);
        }
        &:active{
            background-color: lighten($color: #00f800, $amount: 10);
        }
    }
}

</style>