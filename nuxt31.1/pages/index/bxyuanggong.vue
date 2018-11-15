<template>
  <div class="detail-wrap">
    <div class="box_4">
      <!--第一部 上方搜索框   -->
      <div class="top_1">
        <div class="biaoti">
          <p>报修管理&nbsp&nbsp></p>
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
    <!--红色背景-->
    <div class="top_2" style="width: 1000px;font-weight:bold">
      <p>员工详情</p>
    </div>

    <div class="box_5">
      <div class="top_51">
        <p>维修师傅</p>
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
        </div>
      </div>
      <!--列表开始-->
      <div class="leibiao_1">
        <div style="height: 38px;width:600px ;line-height: 38px;font-size: 16px"><p>报修详情</p></div>
        <div style="margin-left: 16px">
          <div class="leibiao_2">
            <p style="font-size: 14px;color: #666666">报修状态</p>
            <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">等待维修</p>
          </div>
          <div class="leibiao_3">
            <p style="font-size: 14px;color: #666666">房源信息</p>
            <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">翠城馨院1#702-A室</p>
          </div>
          <div class="leibiao_2">
            <p style="font-size: 14px;color: #666666">地理位置</p>
            <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">鄞州区钱湖北路200号</p>
          </div>
          <div class="leibiao_3">
            <p style="font-size: 14px;color: #666666">联系电话</p>
            <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">138 0000 0000</p>
          </div>
          <div class="leibiao_2">
            <p style="font-size: 14px;color: #666666">报修编号</p>
            <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">0000 0001</p>
          </div>
          <div class="leibiao_2">
            <p style="font-size: 14px;color: #666666">报修时间</p>
            <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">2018-7-2 12：30</p>
          </div>
          <div class="leibiao_2">
            <p style="font-size: 14px;color: #666666">报修编号</p>
            <p style="font-size: 14px;color: #AAAAAA;margin-left: 18px">2018-7-4 上午</p>
          </div>
          <!--身份证-->
         </div>
        <div>
          <div style="height: 38px;width:600px ;line-height: 38px;font-size: 16px"><p>报修备注</p></div>
        <div>
          <Input v-model="value8" type="textarea" style="width: 650px;" :autosize="{minRows: 3,maxRows: 3}" placeholder="请输入..." />
        </div>
          <!--/*文件上传开始*/-->
          <div class="wenjian_1">
            <div class="wenjian_2">
              <Upload
                multiple
                type="drag"
                action="//jsonplaceholder.typicode.com/posts/">
                <img src="../../assets/picture/btn_upload_picture_hover.png" alt="">
              </Upload>
            </div>
            <div class="wenjian_3">
              <Upload
                multiple
                type="drag"
                action="//jsonplaceholder.typicode.com/posts/">
                <img src="../../assets/picture/btn_upload_picture_hover.png" alt="">
              </Upload>
            </div>
          </div>
          <!--/*文件上传结束*/-->
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
  .ivu-rate{
    font-size: 25px;
    font-weight: bolder ;
  }
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
    margin-top: 24px;
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
    margin-top: 145px;
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
  /*底部按钮结束*/
  /*文件上传开始*/
  .wenjian_1{
    margin-top: 24px;
    width: 220px;
    height: 96px;
    position: relative;

  } .wenjian_2{
      display: inline-block;
      float: left;
    } .wenjian_3{
        display: inline-block;
        float: left;
        margin-left: 16px;
      }
  /*文件上传结束*/
  /*文件上传开始*/
  .detail-right{
    width:96px !important;
    height: 96px !important;
  }
  .ivu-upload{
    height: 96px !important;
    background-color: #F1F1F1;
  }
  /*文件上传结束*/

</style>
