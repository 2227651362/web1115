<template>
  <div class="detail-wrap">
    <div class="detail-left">
      <div class="product-board">
        <div style="font-size: 25px;color: #dbe1ec">-2018-</div>
        <div style="font-size: 25px;color: #F5F5F5">10月31号</div>
        <ul>
          <li><nuxt-link to="/h1"><p>综合监控</p></nuxt-link></li>
          <li><nuxt-link to="/h2"><p>订单管理</p></nuxt-link></li>
          <li><nuxt-link to="/h3"><p>房源管理</p></nuxt-link></li>
          <li><nuxt-link to="/h4"><p>员工管理</p></nuxt-link></li>
          <li><nuxt-link to="/h5"><p>报修管理</p></nuxt-link></li>
          <li><nuxt-link to="/h6"><p>租客管理</p></nuxt-link></li>
        </ul>
        <div class="button_1">
          <Button style="height: 30px" ><p>我的设置</p></Button>
        </div>
      </div>
    </div>
    <div class="detail-right">
      <keep-alive>
        <router-view></router-view>
      </keep-alive>
    </div>
  </div>
</template>
<script>
  export default {
    name: "hello"
  }
</script>
<style scoped>
  .detail-wrap{
    width: 1250px;
    margin: 0 auto;
    overflow: hidden;
  }
  .detail-left{
    margin:0 0 0 20px ;
    float: left;
    width: 160px;
    text-align: center;
    background-color: #222222;
  }
  .detail-right{
    float: left;
    width: 1000px;
  }
  .product-board{
    padding: 20px 0;
  }
  .product-board ul{
    margin-top: 20px;
  }
  .product-board li{
    text-align:left;
    padding: 15px 15px;
    cursor: pointer;
  }
  .product-board li a{
    text-decoration:none;
  }
  .product-board li p{
    color: #F5F5F5;
    font-size: 20px;
    text-align: center;
  }
  .product-board li.active,
  .product-board li:hover{
    background: #FFB400;
    color: #fff;
  }
  .sales-board li a{
    display: block;
  }
  .sales-board-intro h2{
    font-size: 20px;
    padding: 20px;
  }
  .sales-board-intro p{
    background: #f7fcff;
    padding: 10px 20px;
    color: #999;
    line-height: 1.8;
  }
  .sales-board-des p{
    line-height: 1.6;
  }
  .sales-board-des h2{
    font-size: 20px;
    padding-bottom: 15px;
  }
  .sales-board-des h3{
    font-size: 18px;
    font-weight: bold;
    padding: 20px 0 10px 0;
  }
  .sales-board-des li{
    padding: 5px 0;
  }
  .sales-board-table th{
    background: #4fc08d;
    color: #fff;
  }
  .sales-board-table td{
    border: 1px solid #f0f2f5;
    padding: 15px;
  }
  .button_1{
    margin: 420px 0 16px 0;
    height: 20px;
  }
  .button_1 button{
    line-height: 20px;
    color: #686868;
    background-color:#393939 ;

  }
  .button_1 button p{
    line-height: 20px;
  }
</style>
