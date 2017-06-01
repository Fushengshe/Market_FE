<template>
  <div class = "login">
    <div class = "cover">

    </div>
    <div class = "topBg">

    </div>

    <div class = "round">

    </div>

    <div class = "main">

    </div>


  </div>
</template>

<script>

export default {
  name: 'Login',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{

  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>



  .login{
    height:100rem;
    width:100rem;
    position:relative;
  }

  .topBg{
    position:absolute;
    top:0;
    width:100rem;
    height:65%;
    background-color:red;
  }

  .main{
    position:absolute;
    bottom:-75%;
    width:100%;
    height:120%;
    background-color:green;
  }

  .cover{
    position:absolute;
    top:-8rem;
    bottom:-70rem;
    z-index:99;
  }

  .cover:before{
    content: "";
    display: block;
    height: 9rem;
    width: 9rem;
    border-top: none;
    border-bottom: 105rem #fff solid;
    border-left: transparent 20rem solid;
    border-right: none;
    transform:rotateZ(90deg) scaleY(-1) scale(1.5);
    z-index = 999;
  }

  .round{
    position:absolute;
    top:27rem; left:30%;
    width: 22rem;
    height: 22rem;
    background: green;
    border-radius: 50rem;
    z-index:999;
  }
</style>
