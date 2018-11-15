<template>
  <div class="detail-wrap">
    <div class="box_4">
      <!--第一部 上方搜索框   -->
      <div class="top_1">
        <div class="biaoti">
          <nuxt-link to="/h4"> <p>员工管理&nbsp&nbsp></p></nuxt-link>
        </div>
        <div class="biaoti" style="margin-left: 24px">
          <p>快速搜索&nbsp&nbsp></p>
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
      <!--红色背景-->
      <div class="top_2">
        <p>输入的"员工编号"查找到如下结果</p>
      </div>
      <!--蓝色背景-->
      <div class="content_2">
        <div class="touxiang_1">
          <p>头像</p>
        </div>
        <div class="bankuai_5">姓名</div>
        <div class="bankuai_5">性别</div>
        <div class="bankuai_5">电话</div>
        <div class="bankuai_5">状态</div>
        <div class="bankuai_5">岗位类别</div>
        <div class="bankuai_5">管辖范围</div>
      </div>
      <!--具体数据-->
      <!-- 员工信息列表数据开始-->
      <div class="content_2_2">
        <!--图片存放-->
        <div class="tupian_1">
          <img src="../../assets/picture/ic_avatar_default.png" alt="1213">
        </div>
        <!--具体信息-->
        <div class="bankuai_6">胡杰</div>
        <div class="bankuai_6">女</div>
        <div class="bankuai_6">13800000000</div>
        <div class="bankuai_6">在岗</div>
        <div class="bankuai_6">客户服务</div>
        <div class="bankuai_6">智谷公寓</div>
        <!--<Icon class="tubiao_1" type="ios-create" />-->
      </div>
      <!--结束-->
    </div>
  </div>
</template>

<script>
  export default {
    name: 'xq'

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
  /*<!--第一部分员工管理 结束-->*/
  /*第二部分开始*/
  .top_2{
    height: 40px;

  }
  .top_2 p{
    margin-left: 24px;
    line-height: 40px;
    font-size: 18px;
    color: #222222;
  }
  /*蓝色背景*/
  .content_2{
    width: 976px;
    float: left;
    background-color: #EAF3F8;
  }
  .touxiang_1{
    float: left;
    width: 65px;
    margin-left: 24px;
    line-height: 48px;
    color: #222222;
    font-size: 16px;
  }
  .bankuai_5{
    float: left;
    width: 120px;
    line-height: 48px;
    color: #222222;
    font-size: 16px;
    text-align: center;
  }
  /*第二部 结束*/
  /*具体信息开始*/
  .content_2_2{
    height: 72px;
  }
  .content_2_2 img{
    float: left;
    margin: 12px 24px 0 16px;
  }
  .bankuai_6{
    float: left;
    width: 120px;
    line-height:72px;
    color: #222222;
    font-size: 16px;
    text-align: center;
  }
</style>
