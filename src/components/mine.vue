<template>
  <div class = "Mine">
    <div class = "avatar">
      <img src = "../assets/touxiang.jpg" />
    </div>

    <div class = "main">
      <mt-cell title="个人资料" to="#" is-link>
        <img slot="icon" src="../assets/material.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="我的物品" to="#" is-link>
        <img slot="icon" src="../assets/artical.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="我的小票" to="#" is-link>
        <img slot="icon" src="../assets/receipt.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="客服中心" to="#" is-link>
        <img slot="icon" src="../assets/service.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="设置" to="#" is-link>
        <img slot="icon" src="../assets/setting.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="退出" to="#" is-link>
        <img slot="icon" src="../assets/exit.png" width="24" height="24">
      </mt-cell>
    </div>
   </div>
</template>

<script>
import { Cell } from 'mint-ui';

export default {
  name: 'Mine',
  data () {
    return {

    }
  },
  components:{
    Cell: Cell
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  a{
    text-decoration:none;
  }

  .Mine{
    height:100%;
    width:100%;
  }

  .avatar{
    width:100%;
    height:24vh;
    background-color:#ccc;
    text-align:center;
    padding-top:2vh;
    padding-bottom:2vh;
  }

  .avatar img{
    height:8em;
    width:8em;
  }
</style>
