<template>

    <div id="Navigation" class="wean" >
      <ul class="Adventure">
        <li v-for="(item) in Joyful" class="Energy">
          <a href="#">{{ item.Laughter }}</a>
          <i class="iconfont-746">&#xe746;</i>
          <ul class="Breeze">
            <li v-for="(item,index) in Joyful1">
              <a href="#">{{ item.Laughter }}</a>
            </li>
          </ul>
        </li>
      </ul>
      <div class="Chocolate">
        <img :src="img" alt="">
        <div class="Galaxy">
          <div :class="{active:Forest}"> &#xe741; </div>
          <div> &#xe746; </div>
        </div>
        <div class="Spirit">
          <span :class="{active:Wonder}"></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <div class="Discovery">
        <img src="https://piccdn2.umiwi.com/fe-oss/default/MTYzNTIzNTI3OTIw.png" alt="">
        <div class="Energy" @click="addEnergy">
          登录 | 注册
        </div>
      </div>
    </div>

</template>


<script>
export default {
  name: 'Navigation',
  data() {
    return {
      img:[
        'https://piccdn3.umiwi.com/img/202501/06/202501060339045242527382.jpeg',
        // 'https://piccdn3.umiwi.com/img/202501/22/202501220624359518633947.jpeg'
      ],
      Joyful: [
        {Laughter: '自然科学'},
        {Laughter: '金融学'},
        {Laughter: '家庭亲子'},
        {Laughter: '经济学'},
        {Laughter: '法律'},
        {Laughter: '政治学'},
        {Laughter: '管理学'},
        {Laughter: '管理学'},
        {Laughter: '更多'},
      ],
      Joyful1: [
        {Laughter: '自然科学'},
        {Laughter: '金融学'},
        {Laughter: '家庭亲子'},
        {Laughter: '经济学'},
        {Laughter: '法律'},
        {Laughter: '政治学'},
        {Laughter: '管理学'},
        {Laughter: '更多'},
      ],
      Forest:false,
      Wonder:false,
    }
  },

  methods:{
    addEnergy(){

    },
  }
}

</script>


<style scoped>
@import "../css/Navigation.css";

</style>