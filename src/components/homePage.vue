<template>
  <div class = "homePage">
     <div class="page-wrap">
       <mt-tab-container class="page-tabbar-container" v-model="selected">
         <mt-tab-container-item id="首页">
          <Home></Home>
         </mt-tab-container-item>

         <mt-tab-container-item id="发现">
           <!-- <ProductInfo></ProductInfo> -->
           <!-- <Confirmation></Confirmation> -->
         </mt-tab-container-item>

         <mt-tab-container-item id="购物车">
           <Cart></Cart>
         </mt-tab-container-item>

         <mt-tab-container-item id="我的">
           <Mine></Mine>
           <!-- <Login></Login> -->
           <!-- <ProductInfo></ProductInfo> -->
           <!-- <Confirmation></Confirmation> -->
         </mt-tab-container-item>
       </mt-tab-container>
     </div>



     <mt-tabbar v-model="selected" fixed>
       <mt-tab-item id="首页">
         <img slot="icon" src="../assets/home.png">
         首页
       </mt-tab-item>

       <mt-tab-item id="发现">
         <img slot="icon" src="../assets/find.png">
         发现
       </mt-tab-item>

       <mt-tab-item id="购物车">
         <img slot="icon" src="../assets/cart.png">
         购物车
       </mt-tab-item>

       <mt-tab-item id="我的">
         <img slot="icon" src="../assets/mine.png">
         我的
       </mt-tab-item>
     </mt-tabbar>

 </div>
</template>

<script>
import Mine from './mine'
import Home from './home'
import Cart from './cart'
import Confirmation from './confirmation'
import ProductInfo from './productInfo'
import Login from './Login'

import { Tabbar, TabItem, TabContainer, TabContainerItem} from 'mint-ui';


export default {
  name: 'homePage',
  data () {
    return {
      active: 'tab-container1',
      selected: '首页',
    }
  },
  components:{
    Mine,
    Home,
    Cart,
    Confirmation,
    ProductInfo,
    Login,
    Tabbar: Tabbar,
    TabItem: TabItem,
    TabContainer: TabContainer,
    TabContainerItem: TabContainerItem,
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
