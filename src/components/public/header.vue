<template>
  <div class="header">
    <div><img src="../../assets/logo.png" alt=""></div>
    <div class="search"><Input search placeholder="请搜索" /></div>
    <div class="headRight">
      <div class="imgDiv"><img class="icon1" src="../../assets/history.png" alt=""></div>
      <div class="imgDiv"><img class="icon2" src="../../assets/msg.png" alt=""></div>
      <div class="imgDiv"><img class="icon3" src="../../assets/mine.png" alt=""></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'header',
  data () {
    return {
      message: '1111'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.header {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
}
.imgDiv {
  display: flex;
  justify-content: center;
  align-items: center;
}
.icon3 {
  width: 36px;
  height: 36px;
  margin-left: 12px;
}
.icon1{
  width: 48px;
  height: 48px;
}
.icon2 {
  width: 58px;
  height: 58px;
}
.login {
  display: flex;
  flex-direction: row;
}
.search {
  width: 300px;
}
.ivu-layout-header {
  background: #fff !important;
}
.ivu-input {
  border-radius: 50px !important;
}
.headRight {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
