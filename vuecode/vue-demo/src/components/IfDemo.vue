<template>
    <h3>条件渲染</h3>
    <div v-if="flag">你能看见我吗</div>
    <div v-else>你还是看看我吧</div>
    <div v-if="num==='a'">A</div>
    <div v-else-if="num===b">B</div>
    <div v-else-if="num===c">C</div>
    <div v-else>Not A/B/C</div>
    <div v-show="flag">你真的看见我吗</div>

</template>

<script>
    export default{
        data(){
            return {
                flag: true,//true,
                num:'D'
            }
        }
    }
</script>

<!-- v-if 元素的销毁和重建，较高的切换开销
    v-show 较高的初始开销，无论初始条件如何始终都会渲染，频繁切换时开销小, 切换是基于style属性none-->