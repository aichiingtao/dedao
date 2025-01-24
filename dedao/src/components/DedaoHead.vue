<template>
  <div id="header">
    <div class="header">
      <div class="header-top wean">
        <div class="header-top-img">
          <img src="https://piccdn2.umiwi.com/fe-oss/default/MTYzNzA0MzE4NTgz.png" alt="">
        </div>
        <div class="header-top-Search">
          <div :class="['Search',{active:isActive}]">
            <i class="iconfont-698">&#xe698;</i>
            <input type="text" placeholder="你想学习什么？" @click="add">
            <button>得到一下</button>
          </div>
          <div class="Elephant" v-show="isShow">
            <h5>热门搜索</h5>
            <div>
              <ul>
                <li>
                  <a href="#">
                    <i class="iconfont-660">&#xe660;</i>
                    <h5>万维钢·精英日课6</h5>
                    <p>重磅上新！</p>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <i class="iconfont-660">&#xe660;</i>
                    <h5>AI学习圈</h5>
                    <p>快刀广播站天天聊AI</p>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="header-top-Login">
          <div class="Apple">
            <a>
              <i class="iconfont-8f2">&#xe8f2;</i>
              知识城邦</a>
            <a>
              <i class="iconfont-8f2">&#xe8f2;</i>
              知识城邦
            </a>
          </div>
          <div class="Adventure">
            <i class="iconfont-904">
              &#xe904;
            </i>
            <div class="Breeze">

            </div>
            <div class="Zebra">
              <h3>更新提示</h3>
              <span>
                <p>Hi～<i>朋友</i> </p>
                <p>近期我们新增了以下功能：</p>
              </span>
              <p>① 书架智能分类：可按学习进度和内容类型自动整理</p>
              <p>② 最近学习</p>
              <p>赶紧来学习吧</p>
              <p>欢迎发邮件和我们交流：iget@luojilab.com</p>
            </div>
          </div>
          <div class="Cat-Login">
            <div class="Login" @click="addLogin">
              登录 | 注册
            </div>
            <div class="Banana">
              <h4>登录得到，学习更多内容</h4>
              <ul>
                <li>
                  <i class="iconfont-909">&#xe909;</i>
                  大屏学习
                </li>
                <li>
                  <i class="iconfont-909">&#xe909;</i>
                  大屏学习
                </li>
                <li>
                  <i class="iconfont-909">&#xe909;</i>
                  大屏学习
                </li>
                <li>
                  <i class="iconfont-909">&#xe909;</i>
                  大屏学习
                </li>
              </ul>
              <div @click="addLogin">
                立即登录
              </div>
              <p>首次登录？<a href="#"  @click="addLogin">点我登录</a></p>
            </div>
            <div class="Dog"></div>
          </div>
        </div>
      </div>
    </div>
    <Login v-show="isShow1" @Umbrella="Yacht" @Friendship="Galaxy"></Login>
  </div>

</template>

<script>
import Login from '../views/Login.vue'

export default {
  name: 'header',
  components: {
    Login
  },


  data() {
    return {
      isShow: false,
      isShow1: false,
      isActive: false,
      Energy:false,
    }
  },


  methods: {
    add() {
      if (!this.isShow && !this.isActive) {
        this.isShow = true
        this.isActive = !this.isActive
      }
    },
    // 登录弹窗显示
    addLogin(){
      this.isShow1 = true
      // 登录弹窗显示，5秒之后，手动刷新二维码
      let i = 5
      const Timer = setInterval( () =>{
        i--
        if (i === 0){
          this.$emit('Friendship', true)
          clearInterval(Timer)
          console.log('倒计时刷新二维码')
        }
      },1000)
    },

    Galaxy(){
      console.log(123)
    },


    // 关闭登录窗口
    Yacht(get){
      this.isShow1 = get
    }
  },


}


</script>
<style scoped>

@import '../css/Head.css';

</style>