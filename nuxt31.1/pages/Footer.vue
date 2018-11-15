<template>
  <div class="app-foot">
    <p>这里输入一段文字！！！底部</p>
  </div>
</template>

<script>
  export default {
    name: "footer",
    data(){
      return{

      }
    }
  }
</script>

<style scoped>
  .app-foot{
    text-align: center;
    height: 80px;
    width: 100%;
    line-height: 80px;
    background: #e3e4e8;
    clear: both;
    margin:0 auto;
  }
  .app-foot p{
    display: inline-block;
  }
</style>
