<template>
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
</template>
<script>
  export default {


  }
</script>
<style>
.detail-right{
  width:96px !important;
  height: 96px !important;
}
.ivu-upload{
  height: 96px !important;
  background-color: #F1F1F1;
}
  .wenjian_1{
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
</style>
