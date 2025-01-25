<template>
  <div id="Login" class="Rainbow">
    <div  class="Flower">
      <div class="Tiger" @click="addTiger" >
        <i class="iconfont-674">&#xe674;</i>
      </div>
      <div class="Guitar">
        <h3>验证码登录</h3>
        <div class="Ice">
          <label>+86</label>
          <i class="iconfont-744">&#xe744;</i>
          <input type="text" placeholder='请输入手机号' v-model="number">
        </div>
        <p v-if="iSif">*请输入正确手机</p>
        <div class="Ice">
          <input type="text" placeholder='请输入验证码'>
          <button @click="addVerification">{{ Verification }}</button>
        </div>
        <div class="Journey" @click="addJourney">
          登录
        </div>
        <span class="Kite">
          <input type="checkbox">
          我同意并愿意遵守得到
        </span>
          <span class="Lemon"><a href="#">《用户服务协议》</a>和<a href="#">《隐私政策》</a></span>
      </div>
      <div class="Happiness">
        <h3>扫码登录</h3>
        <span class="Notebook">同时支持「得到App」和「微信」扫码</span>
        <div class="Ocean">
          <img v-if="Illusion" src="data:image/png;base64,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" alt="">
          <img v-else src="data:image/png;base64,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" alt="">
          <div class="Discovery" v-show="Energy">
            <p>二维码已过期 <br>请<button >点击此处</button>刷新</p>
          </div>
        </div>
        <span class="Peace">
          <i :class="['iconfont-762',{active:Harmony}]" @click="add762">&#xe762;</i>
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



export default {
  name:'Login',


  data(){
    return{
      iSif:false,
      number:'',
      Verification:'获取验证码',
      Energy:false,
      Harmony:false,
      Illusion:true
    }

  },

  methods:{
    add762(){
      if(!this.Harmony){
        this.Harmony = true
        this.Illusion = false
      }
      else {
        this.Harmony = false
        this.Illusion = true
      }

    },

    addTiger(){
      this.$emit('Umbrella', false)
      this.iSif = false
      this.Verification = '获取验证码'
    },
    addJourney(){
      if (this.number){
        console.log(111)
      }
      else {
        this.iSif = true
      }
    },
    addVerification(){
      let i = 5
      const closure = setInterval( () =>{
        if( i === 0){
          clearInterval(closure)
          this.Verification = `重新获取`
          console.log('定时器关闭')
        }
        else {
          console.log(123)
          this.Verification = `${i}秒重新获取`
          i--
        }
      },1000)
    },
  }
}

</script>



<style scoped>
@import "../css/Login.css";

</style>