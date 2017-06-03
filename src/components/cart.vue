<template>
  <div class = "cart">
    <div class = "commodity">
      <mt-cell-swipe title="华为p9" to="#productInfo" is-link :right = "btn">
        <img slot="icon" src="#" width="24" height="24">
      </mt-cell-swipe>
      <mt-cell-swipe title="iphone7" to="#" is-link>
        <img slot="icon" src="#" width="24" height="24">
      </mt-cell-swipe>
      <mt-cell-swipe title="小米6" to="#" is-link>
        <img slot="icon" src="#" width="24" height="24">
      </mt-cell-swipe>
      <mt-cell-swipe title="macbook" to="#" is-link>
        <img slot="icon" src="#" width="24" height="24">
      </mt-cell-swipe>
    </div>

  </div>
</template>

<script>
import { CellSwipe } from 'mint-ui';
import ProductInfo from './productInfo'

export default {
  name: 'Home',
  data () {
    return {
      btn:[{
        content: '交换',
        style: { background:'#blue', color: '#fff'},
        // handler:()
      }]
    }
  },
  components:{
    CellSwipe: CellSwipe
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  a{
    text-decoration:none;
  }

  .cart{
    height:100%;
    width:100%;
  }


</style>
