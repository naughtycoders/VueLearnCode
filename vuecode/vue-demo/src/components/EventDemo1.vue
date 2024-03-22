<template>
    <h3>内联事件处理器</h3>
    <!-- <button v-on:click="count++">Add 1</button> -->
    <button @click="count++">Add 1</button>
    <p>count is: {{ count }}</p>
</template>

<script>
    export default{
        data(){
            return {
                count:0,
            }
        }
    }
</script>