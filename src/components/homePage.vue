<template>
  <div class = "homePage">
    <div class="page-tabbar">
       <div class="page-wrap">
         <mt-tab-container class="page-tabbar-container" v-model="selected">
           <mt-tab-container-item id="首页">
            <mt-search v-model="search"></mt-search>
            <mt-swipe>
              <mt-swipe-item>1</mt-swipe-item>
              <mt-swipe-item>2</mt-swipe-item>
              <mt-swipe-item>3</mt-swipe-item>
            </mt-swipe>
           </mt-tab-container-item>
           <mt-tab-container-item id="发现">
             <mt-cell v-for="n in 5" :title="'订单 ' + n" />
           </mt-tab-container-item>
           <mt-tab-container-item id="购物车">
             <mt-cell v-for="n in 7" :title="'发现 ' + n" />
           </mt-tab-container-item>
           <mt-tab-container-item id="我的">
             <div class="page-part">
               <mt-cell v-for="n in 12" :title="'我的 ' + n" />
             </div>
             <router-link to="/">
               <mt-button type="danger" size="large">退出</mt-button>
             </router-link>
           </mt-tab-container-item>
         </mt-tab-container>
       </div>

       <mt-tabbar v-model="selected" fixed>
         <mt-tab-item id="首页">
           <img slot="icon" src="#">
           首页
         </mt-tab-item>
         <mt-tab-item id="发现">
           <img slot="icon" src="#">
           发现
         </mt-tab-item>
         <mt-tab-item id="购物车">
           <img slot="icon" src="#">
           购物车
         </mt-tab-item>
         <mt-tab-item id="我的">
           <img slot="icon" src="#">
           我的
         </mt-tab-item>
       </mt-tabbar>
     </div>
   </div>
</template>

<script>
import { Tabbar, TabItem } from 'mint-ui';
import { TabContainer, TabContainerItem } from 'mint-ui';
import { Search } from 'mint-ui';
import { Swipe, SwipeItem } from 'mint-ui';

export default {
  name: 'homePage',
  data () {
    return {
      active: 'tab-container1',
      selected: '首页',
      search: '',
      auto: 4000
    }
  },
  components:{
    Tabbar: Tabbar,
    TabItem: TabItem,
    TabContainer: TabContainer,
    TabContainerItem: TabContainerItem,
    Search: Search,
    Swipe: Swipe,
    SwipeItem: SwipeItem
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  a{
    text-decoration:none;
  }

  .homePage{
    height:100%;
    width:100%;
  }

</style>
