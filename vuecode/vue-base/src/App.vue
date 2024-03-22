<script>
  export default{
    data(){
      return {
        msg: '模板语法',
        number: 10,
        ok: true,
        message: "大家好啊",
        html: '<a href=https://www.baidu.com/>百度<a>',
      }
    }
  }
</script>

<template>
<h3>神奇的语法</h3>
<p>{{ msg }}</p>
<p>{{ number + 1 }}</p>
<p>{{ ok?'true':'false' }}</p>
<p>{{ message.split('').reverse().join('') }}</p>
<!-- <p>{{ var a = 1 }}</p>
<p>{{ if(ok) return message }}</p> -->
<p>{{ html }}</p>
<p v-html=html></p>
</template>

