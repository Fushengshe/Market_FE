<template>
  <div class = "home">
    <mt-search v-model="search"></mt-search>

    <div class = "swipe">
      <mt-swipe :auto = "4000">
        <mt-swipe-item>12312313</mt-swipe-item>
        <mt-swipe-item>2</mt-swipe-item>
        <mt-swipe-item>3</mt-swipe-item>
      </mt-swipe>
    </div>

    <div class = "infoCell">
      <mt-cell title="数码用品" to="#" is-link>
        <img slot="icon" src="../assets/digital.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="家居用品" to="#" is-link>
        <img slot="icon" src="../assets/household.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="日常用品" to="#" is-link>
        <img slot="icon" src="../assets/daily.png" width="24" height="24">
      </mt-cell>
      <mt-cell title="衣鞋帽裤" to="#" is-link>
        <img slot="icon" src="../assets/clothes.png" width="24" height="24">
      </mt-cell>
    </div>

    <div class = "recom">
      <div class = "recomL">

      </div>

      <div class = "recomR">

      </div>
    </div>
  </div>
</template>

<script>
import { Tabbar, TabItem, TabContainer, TabContainerItem, Search, Swipe, SwipeItem, Cell } from 'mint-ui';

export default {
  name: 'Home',
  data () {
    return {
      search: '',
      auto: '4000'
    }
  },
  components:{
    Tabbar: Tabbar,
    TabItem: TabItem,
    TabContainer: TabContainer,
    TabContainerItem: TabContainerItem,
    Search: Search,
    Swipe: Swipe,
    SwipeItem: SwipeItem,
    Cell: Cell
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  a{
    text-decoration:none;
  }

  .home{
    height:100%;
    width:100%;
  }

  .swipe{
    width:100%;
    height:27vh;
    position:absolute;
    top:3rem;
    z-index:1
    background-color:#888;
  }

  .infoCell{
    width:100%;
    position:absolute;
    top:calc(3rem + 27vh);
    z-index:1
    background-color:#bbb;
  }

  .recom{
    width:100%;
    padding-bottom:em;
    height:calc(100% - ((3rem + 27vh) + 247px));
    position:absolute;
    top:calc((3rem + 27vh) + (48px * 4));
    z-index:1
  }

  .recomL{
    width:49.7%;
    height:100%;
    border-right:1px solid #ddd;
    float:left;
  }

  .recomR{
    width:50%;
    height:100%;
    float:left;
  }

</style>
