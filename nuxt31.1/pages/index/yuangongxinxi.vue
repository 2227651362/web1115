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
        <div class="anniu_6">
          <p>员工公告</p>
        </div>
      </div>
      <!--第一部 结束-->
    </div>
    <!--红色背景-->
    <div class="top_2" style="width: 1000px;font-weight:bold">
      <p>员工详情</p>
    </div>

    <div class="box_5">
      <div class="top_51">
        <p>维修服务（智能公寓）</p>
      </div>
      <!--个人信息与星星存放-->
      <div class="tupian_1">
        <div class="tupian_1l">
          <div class="tupian_1ll">
            <img src="../../assets/picture/ic_avatar_default.png" alt="头像">
          </div>
          <div class="tupian_1lr">
            <div class="tupian_1lr1">
              <p>张志东<img src="../../assets/picture/ic_top_bar_male.png" alt="性别"></p>
            </div>
            <div class="tupian_1lr2">
              <p> <img src="../../assets/picture/ic_contact_number.png" alt="">135 0000 2222</p>
            </div>
          </div>
        </div>
        <div class="xx_1">
          <div class="xx_2">
            <Rate  style="font-weight:900" disabled v-model="valueDisabled" />
          </div>
          <div class="xx_3">
            <p>ID:000 001</p>
          </div>
        </div>
      </div>
      <!--列表开始-->
      <div class="leibiao_1">
        <div style="height: 38px;width:600px ;line-height: 38px;font-size: 16px"><p>基本信息</p></div>
<div style="margin-left: 16px">
  <div class="leibiao_2">
    <p style="font-size: 14px;color: #666666">岗位状态</p>
    <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">在岗</p>
<div class="anniu_4">
<p>切换离岗</p>
</div>
    <!--<Button type="warning;"  class="button_3"><p>切换离岗</p></Button>-->
  </div>
  <div class="leibiao_3">
    <p style="font-size: 14px;color: #666666">权限信息</p>
    <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">维修专用权限</p>
  </div>
  <div class="leibiao_2">
    <p style="font-size: 14px;color: #666666">备注信息</p>
    <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">无</p>
  </div>
  <div class="leibiao_3">
    <p style="font-size: 14px;color: #666666">证件信息</p>
    <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">身份证</p>
  </div>
  <div class="leibiao_2">
    <p style="font-size: 14px;color: #666666">证件号码</p>
    <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">330280199212276154</p>
  </div>
        <!--身份证-->
        <div class="box_6">
          <p style="padding-top: 10px;font-size: 14px;color: #666666; ">证件照片</p>
          <div class="zhengjian_1"  >
            <div class=""  style="background-color: #F7F7F7; width: 220px;height: 150px;border:1px dashed #dbe1ec;">
              <img src="" alt="正面">
            </div>
            <p style="text-align: center">证件正面</p>
          </div>
          <div class="zhengjian_2">
            <div class=""   style="background-color: #F7F7F7; width: 220px;height: 150px;border:1px dashed #dbe1ec;">
              <img src="" alt="背面">
            </div>
            <p style="text-align: center">证件背面</p>
          </div>
        </div>
        <div class="bottom_4">
          <p style="font-size: 14px;color: #666666">维修记录</p>
          <p style="font-size: 14px;color: #FEB63A;margin-left: 18px">等待维修3条</p>
        </div>
  </div>
</div>
        <!--/*底部按钮开始*/-->
        <div class="bottom_5">

          <div class="anniu_1">
            <p>修改分配</p>
          </div>
          <div class="anniu_2">
            <p>撤销报修</p>
          </div>
          <img class="anniu_3" src="../../assets/picture/ic_detail_edit_hover.png" alt="">
        </div>
        <!--结束-->
    </div>
  </div>
</template>
<script>
  export default {
    name: 'xq',
    data () {
      return {
        valueDisabled: 4,
      }
    }
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
  .button_3{
    margin-top: 6px;
    margin-left: 16px;
    display: inline-block;
    position: absolute;
    height: 25px;
    line-height: 10px;
    width: 80px ;
    color: #FD952E;
    text-align: center;
    border: #FFD267  1px  solid;
  }
  .button_3 p {
    color: #FFD267;
    text-align: center;
    margin-left: -8px;
    margin-top: -5px;
  }
  /*<!--第一部分员工管理 结束-->*/

  /*第二部分开始*/
  .top_2{
    height: 48px;
  }
  .top_2 p{
    margin-left: 24px;
    line-height: 48px;
    font-size: 18px;
    color: #666666;
  }
  /*box_5整体部分*/
  .box_5{
    width: 940px;
    margin-left: 36px;

  }
  .top_51{
    height: 38px;
    font-size: 14px;
    line-height: 38px;
  }
  /*星星开始*/
  .tupian_1{
    width: 470px;
    position: relative;
    overflow: hidden;
    height: 80px;
    background-color: #FFFFFF;
    border: 1px solid #dbe1ec;
    border-radius:8px;
  }
  .tupian_1l{
    position: absolute;
    height:80px ;
    width: 280px;
  }

  .tupian_1ll{
    height: 80px;
    width: 80px;

    float: left;
  }
  .tupian_1ll>img{
    margin: 16px 0 16px 20px;
  }
  .tupian_1lr1{
    font-size: 18px;
    margin-top: 16px;
    overflow: hidden;
    position: relative;
  }
  .tupian_1lr1 p{
    font-weight:Bold;
  }
  .tupian_1lr2 p{
    font-size: 14px;
    color: #666666;
  }
  .xx_1{
    height: 80px;
    width: 200px;
    margin-left: 250px;
  }
  .xx_2{
    margin-top: 16px;
    text-align: right;
  }
  .xx_3{
    text-align: right;
  }
  /*星星结束*/
  /*列表开始*/
  .leibiao_2{
    height: 36px;
    width: 600px;
    line-height: 36px;
  }
  .leibiao_2 p{
    display: inline-block;
  }
  .leibiao_3{
    height: 36px;
    width: 600px;
    line-height: 36px;
  }
  .leibiao_3 p{
    display: inline-block;
  }
  /*身份证*/
  .box_6{
    height: 216px;
    width: 600px;
    overflow: hidden;
    position: relative;

  }

  .zhengjian_1{
    margin-left: 80px;
    float: left;
    display: block;
    position: absolute;

  }
  .zhengjian_2{
    margin-left: 310px;
    float: right;
    position: absolute;
    display: block;
  }

  /*结束*/
  .bottom_4{
    height: 36px;
    width: 600px;
  }
  .bottom_4 p{
    line-height: 36px;
    display: inline-block;
  }
  /*底部按钮开始*/
  .bottom_5{
    width: 700px;
    height: 60px;
    position: relative;
    overflow: hidden;
    float: right;
    margin-top: 195px;
    margin-bottom: 24px;
  }
  .anniu_1{
    background: url("../../assets/picture/btn_main_green_normal.png")no-repeat;
    width: 199px;
    height: 60px;
    display: block;
    float: right;
    margin-right: 24px;
    cursor: pointer;
  }
  .anniu_2{
    background: url("../../assets/picture/btn_main_red_normal.png") no-repeat;
    width: 199px;
    height: 60px;
    display: block;
    float: right;
    margin-right: 16px;
    cursor: pointer;
  }
  .anniu_1 p, .anniu_2 p{
    color: white;
    line-height: 60px;
    text-align:center;
    font-size: 25px;
    font-weight: bolder;
  }
  .anniu_3{
float: right;
display: block;
margin-right: 16px;
    margin-top: 8px;
  }
  .anniu_4{
    background: url("../../assets/picture/btn_small_4char_normal.png") no-repeat;
    position: absolute;
    display: inline-block;
    margin-left: 24px;
    line-height: 36px;
    width: 78px;
    height: 24px;
    cursor: pointer;
    margin-top: 6px;
  }
  .anniu_4 p{
    display: table-cell;
    vertical-align:middle;
    line-height: 24px;
    font-size: 15px;
  text-align: center;
    padding-left: 8px;
    color: orange;
  }
  .anniu_6{
    background: url("../../assets/picture/btn_small_4char_normal.png") no-repeat;
    position: absolute;
    display: inline-block;
    margin-left: 145px;
    line-height: 36px;
    width: 78px;
    height: 24px;
    cursor: pointer;
    margin-top: 6px;

  }
  .anniu_6 p{
    display: table-cell;
    vertical-align:middle;
    line-height: 24px;
    font-size: 15px;
    text-align: center;
    padding-left: 8px;
    color: orange;
  }
  /*底部按钮结束*/
</style>
