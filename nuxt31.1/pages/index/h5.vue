<template>
  <div class="detail-wrap">
    <div class="top_1">
      <div class="biaoti">
        <p>保修管理&nbsp></p>
      </div>
      <div class="search">
        <input type="text" class="input_1"   placeholder="   输入员工工号快速查询..."/>
      </div>
      <div>
        <nuxt-link to="/sousuo"> <Button shape="circle" class="button_1"><p>搜索</p></Button></nuxt-link>
      </div>
    </div>
<!--加如标签页-->
    <div class="ui_1">
      <Tabs value="name1">
        <!--标签一 未完成的内容开始-->
        <TabPane label="未完成" name="name1">
          <div class="label_1">
            <div class="lanse_1" style="position: relative;overflow: hidden; width:100%;height:48px;background-color: #EAF3F8  ">
              <p style="margin-left: 24px">保修房源</p>
              <p style="margin-left: 212px">报修备注</p>
              <p style="margin-left: 534px">当前状态</p>
              <p style="margin-left: 700px">预约日期</p>
            </div>
            <div class="label_2" v-for="(item,index) in detailsNav" :class="{on:index%2==0,off:index%2!=0}">
              <p style="margin-left: 24px">{{item.fangyuan}}</p>
              <p style="margin-left: 82px">{{item.beizhu}}</p>
              <p style="margin-left: 130px">{{item.baoxiu}}</p>
              <p style="margin-left: 70px">{{item.riqi}}</p>
              <div class="father1">
                <div class="father2">
                  <nuxt-link  tag="li" to="/bxyuanggong"><img class="tupian_1" :src="item.tupian1" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/bxyuanggong"><img class="tupian_2" :src="item.tupian2" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/bxyuanggong"><img class="tupian_3" :src="item.tupian3" alt=""></nuxt-link>
                </div>
              </div>
            </div>
            <img   @click="handleRender"  class="button_3" src="../../assets/picture/btn_fab_add_normal.png" alt="">
          </div>
        </TabPane>
        <!--  标签一结束   -->
        <!--标签二 已完成的内容开始-->
        <TabPane label="已完成" name="name2">
          <div class="label_1">
            <div class="lanse_1" style="position: relative;overflow: hidden; width:100%;height:48px;background-color: #EAF3F8  ">
              <p style="margin-left: 24px">保修房源</p>
              <p style="margin-left: 212px">报修备注</p>
              <p style="margin-left: 534px">当前状态</p>
              <p style="margin-left: 700px">预约日期</p>
            </div>
            <div class="label_2" v-for="(item,index) in detailsNav" :class="{on:index%2==0,off:index%2!=0}">
              <p style="margin-left: 24px">{{item.fangyuan}}</p>
              <p style="margin-left: 82px">{{item.beizhu}}</p>
              <p style="margin-left: 130px">{{item.baoxiu}}</p>
              <p style="margin-left: 70px">{{item.riqi}}</p>
              <div class="father1">
                <div class="father2">
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_1" :src="item.tupian1" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_2" :src="item.tupian2" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_3" :src="item.tupian3" alt=""></nuxt-link>
                </div>
              </div>
            </div>
            <div class="label_2" v-for="(item,index) in detailsNav" :class="{on:index%2==0,off:index%2!=0}">
              <p style="margin-left: 24px">{{item.fangyuan}}</p>
              <p style="margin-left: 82px">{{item.beizhu}}</p>
              <p style="margin-left: 130px">{{item.baoxiu}}</p>
              <p style="margin-left: 70px">{{item.riqi}}</p>
              <div class="father1">
                <div class="father2">
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_1" :src="item.tupian1" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_2" :src="item.tupian2" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_3" :src="item.tupian3" alt=""></nuxt-link>
                </div>
              </div>
            </div>
            <div class="label_2" v-for="(item,index) in detailsNav" :class="{on:index%2==0,off:index%2!=0}">
              <p style="margin-left: 24px">{{item.fangyuan}}</p>
              <p style="margin-left: 82px">{{item.beizhu}}</p>
              <p style="margin-left: 130px">{{item.baoxiu}}</p>
              <p style="margin-left: 70px">{{item.riqi}}</p>
              <div class="father1">
                <div class="father2">
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_1" :src="item.tupian1" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_2" :src="item.tupian2" alt=""></nuxt-link>
                  <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_3" :src="item.tupian3" alt=""></nuxt-link>
                </div>
              </div>
            </div>
            <img   @click="handleRender"  class="button_3" src="../../assets/picture/btn_fab_add_normal.png" alt="666">
          </div>
        </TabPane>
        <!-- 标签二结束 -->
      </Tabs>
    </div>
    <!--弹出事件开始-->
      <Modal width="680px" v-model="shoeModal">
        <div class="tanchu_1">
          <p style="font-size: 25px">新建报修</p>
          <div class="tanchu_2">
            <div class="tanchu_3" >
              <p>房源报修</p>
              <Input class="input_2" style="width: 240px"  placeholder="房源编号"></Input>
            </div>
            <div class="tanchu_31">
              <p>基本信息</p>
              <div  class="tanchu_4" >
                <Input class="input_2" style="width: 240px"  placeholder="联系电话"></Input>
              </div>
              <div    class="tanchu_5">
                <Select style="width: 240px;" placeholder="预约日期">
                  <Option value="beijing">几月</Option>
                  <Option value="shanghai">几号</Option>
                </Select>
              </div>
            </div>
            <div class="biezhu_1">
              <p>报修备注</p>
              <Input style="width: 580px" type="textarea" :autosize="{minRows: 3,maxRows: 6}"
                     placeholder="说明那个设备需要维修并概述故障问题或现象..." />
            </div>
            <p >报修配图</p>
            <!--/*上传文件开始*/-->
            <div class="deep_1">
              <div class="wenjian_1">
                <div class="wenjian_2">
                  <Upload
                    width="80"
                    multiple
                    type="drag"
                    action="//jsonplaceholder.typicode.com/posts/">
                    <img src="../../assets/picture/btn_upload_picture_hover.png" alt="">
                  </Upload>
                </div>
                <div class="wenjian_3">
                  <Upload
                    width="80"
                    multiple
                    type="drag"
                    action="//jsonplaceholder.typicode.com/posts/">
                    <img src="../../assets/picture/btn_upload_picture_hover.png" alt="">
                  </Upload>
                </div>
              </div>
            </div>
            <!--/*上传文件结束*/-->
          </div>
        </div>
      </Modal>
    <!--弹出事件结束-->
  </div>
</template>
<script>
  export default {
    name: "h8",
    data(){
      return{
        shoeModal:false,
        detailsNav: [
          {
            fangyuan:"泊郁公寓101室",
            beizhu:"墙面明显污损，需要维修。",
            baoxiu:"等待分配",
            riqi:"2018-7-20 18：50",
            tupian1:require("../../assets/picture/btn_small_black_edit_normal.png"),
            tupian2:require("../../assets/picture/btn_small_black_delete_normal.png"),
            tupian3:require("../../assets/picture/btn_small_black_allot_normal.png"),

          },{
            fangyuan:"泊郁公寓101室",
            beizhu:"墙面明显污损，需要维修。",
            baoxiu:"等待分配",
            riqi:"2018-7-20 18：50",
            tupian1:require("../../assets/picture/btn_small_black_edit_normal.png"),
            tupian2:require("../../assets/picture/btn_small_black_delete_normal.png"),
            tupian3:require("../../assets/picture/btn_small_black_allot_normal.png"),

          },{
            fangyuan:"泊郁公寓101室",
            beizhu:"墙面明显污损，需要维修。",
            baoxiu:"等待维修",
            riqi:"2018-7-20 18：50",
            tupian1:require("../../assets/picture/btn_small_black_edit_normal.png"),
            tupian2:require("../../assets/picture/btn_small_black_delete_normal.png"),
            tupian3:require("../../assets/picture/btn_small_black_allot_normal.png"),

          },{
            fangyuan:"泊郁公寓101室",
            beizhu:"墙面明显污损，需要维修。",
            baoxiu:"等待维修",
            riqi:"2018-7-20 18：50",
            tupian1:require("../../assets/picture/btn_small_black_edit_normal.png"),
            tupian2:require("../../assets/picture/btn_small_black_delete_normal.png"),
            tupian3:require("../../assets/picture/btn_small_black_allot_normal.png"),

          },{
            fangyuan:"泊郁公寓101室",
            beizhu:"墙面明显污损，需要维修。",
            baoxiu:"等待维修",
            riqi:"2018-7-20 18：50",
            tupian1:require("../../assets/picture/btn_small_black_edit_normal.png"),
            tupian2:require("../../assets/picture/btn_small_black_delete_normal.png"),
            tupian3:require("../../assets/picture/btn_small_black_allot_normal.png"),

          },{
            fangyuan:"泊郁公寓101室",
            beizhu:"墙面明显污损，需要维修。",
            baoxiu:"等待维修",
            riqi:"2018-7-20 18：50",
            tupian1:require("../../assets/picture/btn_small_black_edit_normal.png"),
            tupian2:require("../../assets/picture/btn_small_black_delete_normal.png"),
            tupian3:require("../../assets/picture/btn_small_black_allot_normal.png"),
          },
        ]
      }
    },
    methods:{
      handleRender () {
        this.shoeModal = true
      }
    }
  }
</script>
<style scoped>
  .detail-wrap{
    width: 1000px;
    position: relative;
    overflow: hidden;
   height: 950px;
  }
  /*<!--第一部分员工管理-->*/
  .top_1{
    margin-left: 20px;
    position: relative;
    overflow: hidden;
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
    margin-left: 420px;
    position: relative;
  }
  /*<!--第一部分员工管理 结束-->*/
.label_1{
  width: 952px;
  margin-left: 24px;
  height: 860px;
}
.lanse_1 p{
  line-height: 48px;
  float: left;
  display: inline-block;
  position: absolute;
  font-size: 16px;
  color: #222222;
}
.label_2{
  width: 952px;
  background-color: #ffffff;
  position: relative;
  float: left;
}
  .label_2 p{
    line-height: 48px;
    float: left;
    display: inline-block;
    font-size: 16px;
  }
.label_2 li{
  display: inline-block;
  line-height: 48px;
  height: 48px;
  width: 24px;
}
  .father1 {
    float: right;
    padding-right: 12px;
    display: none;
  }
  .label_2:hover .father1{
    display: block;
  }
.button_3{
  position:fixed;
  margin-top: 670px;
  margin-left: -100px;
}
/*隔行变色*/
  .on {
    background: #ffffff;
  }
  .off {
    background: #F8F8F8;
  }
/*弹出窗口*/
  .tanchu_1{
    position: relative;
    overflow: hidden;
    font-size: 20px;
  }
  .tanchu_2{
    margin-left: 24px;
    margin-bottom: 12px;

  }
.tanchu_3{
  margin-top: 24px;
  position: relative;
  overflow: hidden;
}
  .tanchu_31{
    margin-top: 12px;
    position: relative;
    overflow: hidden;
  }
  .tanchu_4{
  display: inline-block;
    float: left;
}.tanchu_5{
  display: inline-block;
    float: left;
    margin-left: 16px;
}
 .biezhu_1{
   margin: 12px 0 12px 0;
 }
/*上传文件开始*/

  .deep_1 >>> .detail-right{
    width:96px;
    height: 96px ;

  }
  .deep_1 >>> .ivu-upload{
    height: 96px;
    background-color: #F1F1F1;
  }

  .deep_1 >>> .wenjian_1{
    width: 250px;
    height: 96px;
    position: relative;
    overflow: hidden;
  }
  .deep_1 >>>.wenjian_2{
      display: inline-block;
      float: left;
        height: 96px;
    }
  .deep_1 >>>.wenjian_3{
        display: inline-block;
        float: left;
        margin-left: 16px;

      }
/*上传文件结束*/
  /*深度选择器开始*/
  .ivu-tabs-nav-scroll{
    margin-left: 48px !important;
    font-weight:900 !important;
  }
  /*上传文件开始*/
  .detail-right{
    width:96px !important;
    height: 96px !important;
  }
  .ivu-upload{
    height: 96px !important;
    background-color: #F1F1F1;
  }
  /*上传文件结束*/
  /*ui样式改动开始*/
  .ui_1{
    min-width: 1000px;
  }
  .ui_1 >>> .ivu-tabs-nav .ivu-tabs-tab-active{
    font-size: 20px;
    color: #FFB400;
  }
  .ui_1  >>> .ivu-tabs-nav .ivu-tabs-tab:hover{
    color: #FFB400;
  }
  .ui_1  >>>  .ivu-tabs-nav-container:focus .ivu-tabs-tab-focused{
    color: #FFB400;
  }
  .ui_1 >>> .ivu-tabs-ink-bar{
    color: #FFB400 !important;
    width: 55px !important;
    background-color:#FFB400 !important ;
    margin-left: 20px !important;
  }
  .ui_1  >>> .ivu-tabs-nav .ivu-tabs-tab{
    font-size: 20px;
    margin-left: 0px;
    font-weight: bolder;
  }
  .ivu-btn-primary {
    background-color: #FFB400 !important;
    border-color:#FFB400 !important;
    width: 100px;
    font-size: 14px;
  }
  .ivu-btn-text{
    width: 100px;
    border-color:#dbe1ec !important;
    font-size:14px;
  }
  .ui_1  >>>  .ivu-tabs-nav{
    margin-left: 30px;
  }
</style>
<style>

</style>
