<template>
  <div class = "login">
    <div class = "cover">

    </div>

    <div class = "topBg">

    </div>

    <div class = "round">
      <p>自推荐</p>
    </div>


    <div class = "main">

      <form>
        <div>
          <mt-field class = "username" placeholder="请输入用户名" v-model="username"></mt-field>
          <mt-field placeholder="请输入密码" type="password" v-model="password"></mt-field>
          <mt-field placeholder="验证码" v-model="captcha">
            <img src="#" height="45px" width="100px">
          </mt-field>
        </div>

        <a class = "forgetpsd" href="#">忘记密码</a>
        <mt-button type="default submit"  class = "btnIn">登 录</mt-button>
      </form>

      <p class = "logUp">还没有账号？ <a href="#">注册</a></p>
    </div>


  </div>
</template>

<script>
import { Field } from 'mint-ui';
import { Button } from 'mint-ui';

export default {
  name: 'Login',
  data () {
    return {
      username: '',
      password: '',
      captcha: ''
    }
  },
  components:{MField: Field, MButton: Button}
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  a{
    text-decoration:none;
  }

  .login{
    height:100%;
    width:100%;
    display:flex;
  }

  .topBg{
    width:100%;
    height:38%;
    background-color:red;
  }

  .main{
    position:absolute;
    bottom:0;
    width:100%;
    height:62%;

  }

  /*.cover{

    z-index:99;
    width:0;
  }

  .cover:before{
    position:absolute;
    bottom:calc(-30%);
    content: "";
    display: block;
    height: 0vh;
    width: 0;
    border-bottom: 90rem  solid;
    border-left: transparent 8rem solid;
    transform:rotateZ(90deg) scaleY(-1) scale(2);
    z-index = 999;
  }*/

  .round{
    width: 15vh;
    height: 15vh;
    background-color:rgb(221, 59, 68);
    position:absolute;
    top:23%; right:calc(50% - 7.5vh);
    border-radius: 20rem;
    z-index:999;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:18px;
    color:#fff;
  }

  form{
    margin-top:4rem;
  }

  .forgetpsd{
    display:block;
    text-decoration:none;
    color:#333;
    font-size:12px;
    margin-top:1em;
    padding-right:3em;
    text-align:right;
  }

  .btnIn{
    color:#ddd;
    width:84vw;
    margin:2rem 0 1vh 8vw;
    background-color:rgb(221, 59, 68);
  }

  .logUp{
    text-align:center;
    color:#777;
    font-size:12px;
    margin-top:1rem;
  }

  .logUp a{
    color: #444;
  }
</style>
