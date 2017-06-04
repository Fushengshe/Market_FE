<template>
  <div class = "productInfo">
    <div class = "imgWrapper">
      <img src = "#"/>
    </div>

    <div class = "info">
      <mt-cell title="购买日期" value="2015.06.17"></mt-cell>
      <mt-cell title="是否损坏" value="屏幕有轻微划痕"></mt-cell>
      <mt-cell title="配件是否齐全" value="齐全"></mt-cell>
      <mt-cell title="所在地区" value="河北秦皇岛"></mt-cell>
      <mt-cell :title = "tel">
        <span><mt-button type="default">拨打电话 ></mt-button></span>
        <img slot="icon"  src="#" width="48" height="48"/>
      </mt-cell>
    </div>

    <div class = "btn">
      <mt-button type="default" class = "btnAdd">加入购物车</mt-button>
      <mt-button type="default" class = "btnChan">立即购买</mt-button>
    </div>

  </div>
</template>

<script>
import { Cell, Button } from 'mint-ui'

export default {
  name: 'ProductInfo',
  data () {
    return {
      tel: '133XXXXXXXX'
    }
  },
  components:{
    Cell: Cell,
    Button: Button
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  a{
    text-decoration:none;
  }

  .productInfo{
    height:100%;
    width:100%;
  }

  .imgWrapper{
    height:14em;
  }

  .imgWrapper img{
    width:100%;
    height:100%;
  }

  .btn{
    position:fixed;
    bottom:55px;
  }

  .btnChan, .btnAdd{
    color:#fff;
    border:none;
    border-radius:0;
    margin:0 -4px 0 0;
    width:50vw;
    box-shadow:none;
  }

  .btnChan{
    background-color:rgb(255, 59, 68);
  }

  .btnAdd{
    background-color:rgb(46, 195, 231);
  }
</style>
