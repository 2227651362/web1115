<template>

  <div class="detail-wrap">
    <div class="box_4">
      <!--第一部 上方搜索框   -->
      <div class="top_1">
        <div class="biaoti">
          <nuxt-link to="/h4"> <p>员工管理&nbsp&nbsp></p></nuxt-link>
        </div>
        <div class="biaoti" style="margin-left: 24px;">
          <p>员工详情&nbsp&nbsp></p>
        </div>
        <div class="search">
          <input type="text" class="input_1"   placeholder="   输入员工工号快速查询..."/>
        </div>
        <div>
          <Button shape="circle" class="button_1"><p>搜索</p></Button>
        </div>
        <Button type="warning;"  class="button_2"><p>员工公告</p></Button>
      </div>
      <!--第一部 结束-->
    </div>
    </div>
</template>

<script>
  export default {
    name: "h789"
  }
</script>

<style scoped>
  .detail-wrap{
    min-width: 1000px;
    overflow: hidden;
    position: relative;
  }
  .box_4{
    width: 976px;
    margin-left: 24px;
  }
  .top_1{
    overflow: hidden;
    position: relative;
    height: 35px;
    line-height: 35px;
    border: 1px solid  #F9F9F9;
    background-color: #FFFFFF;
  }
  .top_1 div{
    float: left;
    display: inline-block;
  }
  .search{
    position: relative;
    width: 200px;
    height: 25px;
    border-radius:50px;
  }
  .input_1{
    width: 200px;
    height: 25px;
    border:1px solid #EDE7F3;
    border-radius:15px ;
    opacity: .5;
  }
  .button_1{
    opacity: .7;
    margin-left: 10px;
    background-color: #F8F8F8;
    height: 25px;
    width: 50px;
    display: inline-block;
    line-height: 10px;
  }
  .button_1 p{
    margin-left: -3px;
  }
  .search{
    margin-left: 300px;
    position: relative;
  }
  .button_2{
    float: right;
    margin-right: 24px;
    margin-top: 8px;
    color: #FFB400;
    height: 20px;
    line-height: 20px;
    text-align: center;
    width: 60px;

    border: 1px solid #FFB400;
  }
  .button_2 p{
    text-align: center;
    margin-left: -10px;
    margin-top: -5px;
  }
</style>
