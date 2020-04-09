<template>
    <div>
        <button @click="status= !status">Change Status</button><span class="title">{{status}}</span>
    </div>
</template>

<script>
export default {
    data:() => {
        return {
            status:false
        }
    }
}
</script>
<style>
    .title{
    color:blue;
    }

</style>