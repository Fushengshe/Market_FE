<template>
  <div class = "confirmation">
    <div class = "header">
      <p>购买信息确认</p>
    </div>

    <div class = "tabPanel">
      <div class = "tabGroup1">
        <mt-cell class = "parents" @click.native = "toggle1()" :title = parentItems[0]>
        </mt-cell>
        <div class = "chidren" v-show = "flag1">
          <ul>
            <li v-for = "item in childItems"><mt-cell :title = item.title :value=item.value></mt-cell></li>
          </ul>
        </div>
      </div>

      <div class = "tabGroup2">
        <mt-cell class = "parents" @click.native = "toggle2()" :title = parentItems[1]>
        </mt-cell>
        <div class = "chidren" v-show = "flag2">
          <ul>
            <li v-for = "item in childItems"><mt-cell :title = item.title :value=item.value></mt-cell></li>
          </ul>
        </div>
      </div>


    </div>
  </div>
</template>

<script>
import { Cell } from 'mint-ui';


export default {
  name: 'Confirmation',
  data () {
    return {
      flag1: true,
      parentItems: ["华为p9全新", "相应交换物品", "选择收货地址"],
      childItems: [{
        title: "购买日期",
        value: "2017.05.17"
      },
      {
        title: "是否损坏",
        value: "屏幕有轻微划痕"
      },
      {
        title: "配件是否齐全",
        value: "齐全"
      },
      {
        title: "所在地区",
        value: "河北秦皇岛"
      },
    ]
    }
  },
  methods:{
    toggle1:function(){
      this.flag1 = !this.flag1;
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

  ul, li{
    list-style:none;
  }

  .confirmation{
    height:100%;
    width:100%;
  }

  .tabPanel{
    height:100%;
  }


</style>
