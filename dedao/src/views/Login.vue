<template>
  <div id="Login" class="Rainbow" v-show="isShow" @Sunshine="Rainbow">
    <div  class="Flower">
      <div class="Guitar">
        <h3>验证码登录</h3>
        <div class="Ice">
          <label>+86</label>
          <i class="iconfont-744">&#xe744;</i>
          <input type="text" placeholder='请输入手机号'>
        </div>
        <div class="Ice">
          <input type="text" placeholder='请输入验证码'>
          <label>获取验证码</label>
        </div>
        <div class="Journey">
          登录
        </div>
        <span class="Kite"><input type="checkbox">我同意并愿意遵守得到</span>
          <span class="Lemon"><a href="#">《用户服务协议》</a>和<a href="#">《隐私政策》</a></span>
      </div>
      <div class="Happiness">
        <h3>扫码登录</h3>
        <span class="Notebook">同时支持「得到App」和「微信」扫码</span>
        <div class="Ocean">
          <img src="data:image/png;base64,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" alt="">
        </div>
        <span class="Peace">
          <i class="iconfont-762">&#xe762;</i>
          30天内自动登录
        </span>
        <div class="Mountain">
          <img src="https://piccdn2.umiwi.com/fe-oss/default/MTYzNzMwNzUyMzQy.png" alt="">
        </div>
      </div>

    </div>
  </div>

</template>

<script>

import Bus from '../utils/EventBus'
export default {
  name:'Login',
  data(){
    return{
      isShow:false
    }
  },
  methods:{
    // Rainbow接收到的值，Rainbow = get
    Rainbow(get){
      this.isShow = get
    }
  }
}




</script>



<style scoped>
@import "../css/Login.css";

</style>