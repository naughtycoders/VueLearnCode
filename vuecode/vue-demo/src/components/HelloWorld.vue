<script >
  export default{
    data() {
      return {
        msg:'hello world!',
        dynamicid: 'appid',
        dynamictitle: 'hello',//null,//undefined,
        dynamicclass: 'appclass',
        isbuttondisable: true,
        objectofattrs:{
          id:'appid',
          class:'appclass'
        }
      }
    }
  }
</script>

<template>
  <div :id='dynamicid' v-bind:class='dynamicclass' v-bind:title='dynamictitle'>{{ msg }}</div>
  <button :disabled="isbuttondisable">Button</button>
  <div v-bind="objectofattrs">测试仪</div>
</template>

<style>
.appclass{
  color:red;
  font-size: 30px;
}
</style>