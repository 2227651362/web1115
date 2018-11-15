<template>
  <div class="detail-wrap">
    <div class="box_5">
      <!--第一部 上方搜索框   -->
      <div class="top_1">
        <div class="biaoti">
          <nuxt-link to="/h4"> <p>员工管理&nbsp&nbsp></p></nuxt-link>
        </div>
        <div class="search">
          <input type="text" class="input_1"   placeholder="   输入员工工号快速查询..."/>
        </div>
        <div>
          <nuxt-link to="/sousuo"> <Button shape="circle" class="button_1"><p>搜索</p></Button></nuxt-link>
        </div>
        <div class="anniu_6">
          <p>员工公告</p>
        </div>
        <!--<Button type="warning;"  class="button_2"><p>员工公告</p></Button>-->
      </div>
      <!--第一部 结束-->
    </div>
    <!--第一部 结束-->
    <!--第二部分标题信息 开始-->
    <div class="box_3">
      <div class="top_2">
        <div class="content_2">
          <div class="touxiang_1">
            <p>头像</p>
            <!--第二部分内容-->
          </div>
          <div class="bankuai_5">姓名</div>
          <div class="bankuai_5">性别</div>
          <div class="bankuai_5">电话</div>
          <div class="bankuai_5">状态</div>
          <div class="bankuai_5">岗位类别</div>
          <div class="bankuai_5">管辖范围</div>
        </div>
      </div>
      <!--第二部分结束-->
      <!--员工信息存放 遍历 -->
      <div class="content_2_1">
        <!-- 员工信息列表数据开始     v-for  -->
        <!--:class="['index-board-'+item.id,{'line-last':index%2 !== 0 }]"-->
        <div class="content_2_2" v-for="(item,index) in detailsNav" :class="{on:index%2==0,off:index%2!=0}" :key="index">
          <!--图片存放-->
          <div class="tupian_1">
            <img :src="item.touxiang" alt="1213">
          </div>
          <!--具体信息-->
          <div class="bankuai_6">{{item.xingming}}</div>
          <div class="bankuai_6">{{item.xingbie}}</div>
          <div class="bankuai_6">{{item.dianhua}}</div>
          <div class="bankuai_6">{{item.zhuangtai}}</div>
          <div class="bankuai_6">{{item.gangwei}}</div>
          <div class="bankuai_6">{{item.guanxia}}</div>
          <!--<Icon class="tubiao_1" type="ios-create" />-->
          <nuxt-link  tag="li" to="/yuangongxinxi"><img class="tupian_2" src="../../assets/picture/btn_small_black_edit_hover.png" alt=""></nuxt-link>
        </div>
      </div>
      <!--<Button   @click="handleRender"   type="primary" shape="circle" icon="md-add"  class="button_guding"></Button>-->
      <div class="">
        <img   @click="handleRender"  class="button_3" src="../../assets/picture/btn_fab_add_normal.png" alt="">
      </div>
    </div>
    <Modal
      width="680"
      v-model="shoeModal" >
      <div class="Modal_1">
        <p>添加员工</p>
      </div>
      <div class="box_2">
        <div class="Modal_2">
          <p>员工工号</p>
        </div>
        <div class="Modal_3">
          <p>000&nbsp&nbsp001</p>
        </div>
        <div  style="overflow: hidden;">
          <div class="Modal_2"  style="margin-top:8px">
            <p>员工信息</p>
          </div>
          <div class="xinxi_1">
            <div class="xingxi_left">
              <div class="xingxi_left1">
                <div>
                  <Input class="input_2" style="width: 80px" v-model="formValidate.name" placeholder="姓名"></Input>
                </div>
                <div>
                  <Select style="width: 70px;" v-model="formValidate.city" placeholder="性别">
                    <Option value="beijing">男</Option>
                    <Option value="shanghai">女</Option>
                  </Select>
                </div>
                <div>
                  <Input v-model="formValidate.mail" style="width: 200px; " placeholder="手机号码*"></Input>
                </div>
              </div>
              <div class="xingxi_left2">
                <div class="xingxi_left21" style="width: 166px;padding-top: 9px">
                  <Select v-model="formValidate.city" placeholder="证件类型">
                    <Option value="beijing">身份证</Option>
                    <Option value="shanghai">户口本</Option>
                  </Select>
                </div>
                <div class="xingxi_left22">
                  <Input v-model="formValidate.mail" style="width: 200px; " placeholder="证件号码*"></Input>
                </div>
              </div>
            </div>
<!--文件上传开始-->
            <div class="wenjian_a">
              <div class="wenjian_1">
                <div class="wenjian_2">
                  <Upload
                    multiple
                    type="drag"
                    action="//jsonplaceholder.typicode.com/posts/">
                    <p style="font-size: 30px">+</p>
                    <p>证件正面</p>
                  </Upload>
                </div>
                <div class="wenjian_3">
                  <Upload
                    multiple
                    type="drag"
                    action="//jsonplaceholder.typicode.com/posts/">
                    <p style="font-size: 30px">+</p>
                    <p >证件背面</p>
                  </Upload>
                </div>
              </div>
            </div>
            <!--文件上传结束-->
          </div>
        </div>
        <div style="overflow: hidden;">
          <div class="Modal_2"  >
            <p> 岗位信息</p>
          </div>
          <div class="xinxi_2" style="width: 166px;">
            <Select v-model="formValidate.city" placeholder="岗位类别">
              <Option value="beijing">身份证</Option>
              <Option value="shanghai">户口本</Option>
            </Select>
          </div>
          <div class="xinxi_3" style="width: 166px;">
            <Select v-model="formValidate.city" placeholder="管辖范围">
              <Option value="beijing">身份证</Option>
              <Option value="shanghai">户口本</Option>
            </Select>
          </div>
        </div>
        <div style="overflow: hidden;">
          <div class="Modal_2" style="margin-top:8px">
            <p>其他信息</p>
          </div>
          <div class="xinxi_2" style="width: 166px;">
            <Select v-model="formValidate.city" placeholder="服务星级">
              <Option value="beijing">身份证</Option>
              <Option value="shanghai">户口本</Option>
            </Select>
          </div>
          <div>
            <Input class="input_3" style="width: 432px;margin-left: 16px;" v-model="formValidate.xinxi" placeholder="备注信息"></Input>
          </div>
        </div>
        <div style="overflow: hidden;">
          <div class="Modal_2" style="margin-top:8px">
            <p>权限管理</p>
          </div>
          <div  class="box_4" >
            <div    style="width: 150px;height: 30px;  float: left;">
              <div style="float: left">
                <Radio v-model="single" > 权限管理1</Radio>
              </div>
            </div>
            <div style="width: 128px;height: 30px;  float: left;margin-left: 16px">
              <div style="float: left">
                <Radio v-model="single" > 权限管理2</Radio>
              </div>
            </div>
            <div style="width: 128px;height: 30px;  float: left;margin-left: 16px">
              <div style="float: left">
                <Radio v-model="single"  > 权限管理3</Radio>
              </div>
            </div>
          </div>
        </div>
      </div>
    </Modal>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        value: '',
        modal1: false,
        loading: true,
        shoeModal: false,
        formValidate: {
          name: '',
          mail: '',
          city: '',
          gender: '',
          interest: [],
          date: '',
          time: '',
          desc: '',
          xinxi:'',
        },  detailsNav:[
          {
            touxiang:require("../../assets/picture/ic_avatar_default.png"),
            xingming:"胡杰",
            xingbie:"女",
            dianhua:"13800000000",
            zhuangtai:"在岗",
            gangwei:"客户服务",
            guanxia:"智谷公寓",
          }, {
            touxiang:require("../../assets/picture/ic_avatar_default.png"),
            xingming:"胡杰",
            xingbie:"女",
            dianhua:"13800000000",
            zhuangtai:"在岗",
            gangwei:"客户服务",
            guanxia:"智谷公寓",
          }, {
            touxiang:require("../../assets/picture/ic_avatar_default.png"),
            xingming:"胡杰",
            xingbie:"女",
            dianhua:"13800000000",
            zhuangtai:"在岗",
            gangwei:"客户服务",
            guanxia:"智谷公寓",
          }, {
            touxiang:require("../../assets/picture/ic_avatar_default.png"),
            xingming:"胡杰",
            xingbie:"女",
            dianhua:"13800000000",
            zhuangtai:"在岗",
            gangwei:"客户服务",
            guanxia:"智谷公寓",
          }, {
            touxiang:require("../../assets/picture/ic_avatar_default.png"),
            xingming:"胡杰",
            xingbie:"女",
            dianhua:"13800000000",
            zhuangtai:"在岗",
            gangwei:"客户服务",
            guanxia:"智谷公寓",
          }, {
            touxiang:require("../../assets/picture/ic_avatar_default.png"),
            xingming:"胡杰",
            xingbie:"女",
            dianhua:"13800000000",
            zhuangtai:"在岗",
            gangwei:"客户服务",
            guanxia:"智谷公寓",
          },
        ],
        ruleValidate: {
          xinxi:[{
            required: true, message: 'The name cannot be empty', trigger: 'blur'
          }],
          name: [
            { required: true, message: 'The name cannot be empty', trigger: 'blur' }
          ],
          mail: [
            { required: true, message: 'Mailbox cannot be empty', trigger: 'blur' },
            { type: 'email', message: 'Incorrect email format', trigger: 'blur' }
          ],
          city: [
            { required: true, message: 'Please select the city', trigger: 'change' }
          ],
          gender: [
            { required: true, message: 'Please select gender', trigger: 'change' }
          ],
          interest: [
            { required: true, type: 'array', min: 1, message: 'Choose at least one hobby', trigger: 'change' },
            { type: 'array', max: 2, message: 'Choose two hobbies at best', trigger: 'change' }
          ],
          date: [
            { required: true, type: 'date', message: 'Please select the date', trigger: 'change' }
          ],
          time: [
            { required: true, type: 'string', message: 'Please select time', trigger: 'change' }
          ],
          desc: [
            { required: true, message: 'Please enter a personal introduction', trigger: 'blur' },
            { type: 'string', min: 20, message: 'Introduce no less than 20 words', trigger: 'blur' }
          ]
        }
      }
    },
    methods: {
      handleSubmit (name) {
        this.$refs[name].validate((valid) => {
          if (valid) {
            this.$Message.success('Success!');
          } else {
            this.$Message.error('Fail!');
          }
        })
      },
      handleReset (name) {
        this.$refs[name].resetFields();
      },
      handleRender () {
        this.shoeModal = true
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
  .box_5{
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
    margin-left: 400px;
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
  /*<!--第二部分头像开始......-->*/
  .box_3{
    min-width: 900px;
    position: relative;
    display: inline-block;
height: 100%;
  }
  .top_2{
    height: 48px;
    width: 1000px;
  }
  .content_2{
    float: left;
    background-color: #EAF3F8;
    margin-left: 24px;
    width:952px ;
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
  /*<!--第二部分遍历结束结束......-->*/
  /*员工信息开始*/
  .content_2_1{
    height: 100%;
    width: 1000px;
  }
  .content_2_2{
    width: 952px;
    background-color: #ffffff;
    margin-left: 24px;
    height: 72px;
  }
  .tupian_1 img{
    float: left;
    margin: 12px 24px 0 16px;
  }
  /*放入显示，离开失效*/
  .content_2_2 li{
    display: inline-block;
    width: 144px;
    height:72px;
  }
  .tupian_2{
    display: none;
    float: right;
    margin: 28px 24px 0 0 ;

  }
  .content_2_2:hover .tupian_2{
    display: block;
  }
/*结束*/
  .bankuai_6{
    float: left;
    width: 120px;
    line-height:72px;
    color: #222222;
    font-size: 16px;
    text-align: center;
  }
  /*员工信息图片图片*/
  .Modal_1{
    font-size: 25px;
  }
  .Modal_2{
    font-size: 18px;
    height: 36px;
    line-height: 36px;
  }
  .box_2{
    margin-top: 24px;
    margin-left: 16px;

  }
  .Modal_3{
    width: 168px;
    height: 36px;
    background-color: #F7F7F7;
    line-height: 36px;
    padding-left: 16px;
    font-size: 16px;
  }
  /*弹出窗口*/
  .xinxi_1{
    position: relative;
  }
  .xingxi_left{
    width: 400px;
    position: relative;
    float: left;
  }
  .xinxi_right{
    position: relative;
    width: 232px;
    background-color: #ffffff;
    float: left;
    overflow: hidden;
  }
  .xinxi_right1{
    width: 82px;
    height: 82px;
    float: left;
    background-color: orange;
    margin-left: 16px;
  }
  .xinxi_right2{
    float: left;
    background-color: orange;
    width: 82px;
    height: 82px;
    margin-left: 16px;
  }
  .xingxi_left1{
    height: 200px;
  }
  .xingxi_left1,xingxi_left2{
    position: relative;
    overflow: hidden;
    width: 100%;
    height: 40px;
  }
  .xingxi_left1 div{
    float: left;
    position: relative;
    overflow: hidden;
    height: 40px;
    margin-right: 8px;
  }
  .xingxi_left2 div{
    float: left;
    position: relative;
    overflow: hidden;
    height: 50px;
    line-height: 50px;
  }
  .xingxi_left22{
    margin-left: 16px;
    margin-right: 16px;
  }
  .xinxi_2,.xinxi_3{
    float: left;
    position: relative;
    display: inline-block;
    overflow: hidden;

  }
  /*#div1:after{content:"";clear: both;display: block;}*/
  .xinxi_3{
    margin-left: 16px;
  }
.box_4{
  display: inline-block;
  position: relative;
  width: 600px;
  height: 50px;
}
  .box_4 div{
    margin-left: 8px;
  }
/*隔行变色*/
  .on {
    background: #ffffff;

  }
  .off {
    background: #F8F8F8;

  }
/*文件上传开始*/
  .wenjian_1{
    width: 220px;
    position: relative;
    overflow: hidden;
  } .wenjian_2{
    width: 96px;
    background: url("../../assets/picture/btn_upload_picture_hover.png") no-repeat;
      display: inline-block;
      float: left;
    } .wenjian_3{
     background: url("../../assets/picture/btn_upload_picture_hover.png")no-repeat;
         width: 96px;
        display: inline-block;
        float: left;
        margin-left: 16px;
      }
.wenjian_1 p{
  color:#C5C8CE ;
}

  .button_3{
   float: right;
   display: block;
    position: relative;
    margin-right: 24px;
    margin-bottom: 48px;
   margin-top: 320px;
  }
/*深度选择器开始*/
  .wenjian_a >>> .detail-right{
    width:96px !important;
    height: 86px !important;
  }
  .wenjian_a  >>>.ivu-upload{
    height: 86px !important;
    background-color: #F1F1F1;
  }
  .wenjian_a  >>> .wenjian_1{
    width: 220px;
    height: 86px;
    position: relative;

  }.wenjian_a >>> .wenjian_2{
     display: inline-block;
     float: left;
   } .wenjian_3{
       display: inline-block;
       float: left;
       margin-left: 16px;
     }

  /*文件上传*/
  .ivu-radio-wrapper{
    font-size: 16px;
  }
  .biaoti a{
    color: #666666;
    text-decoration:none;
  }
  .ivu-upload-drag{

  }
  .detail-right{
    width:96px;
    height: 86px ;

  }
  .ivu-upload{
    height: 86px;
    background-color: #F1F1F1;
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
</style>
<style>

</style>
