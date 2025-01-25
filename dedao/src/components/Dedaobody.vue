<template>
  <div>
    <div id="Navigation" class="wean">
      <ul class="Adventure">
        <li v-for="(item) in Joyful" class="Light">
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
        <img :src="img[index1]" alt="">
        <div class="Galaxy">
          <button :class="{active:Forest}" @click="index1--" :disabled="index1 <= 0"> &#xe741;</button>
          <button @click="index1++" :disabled="index1 >= img.length - 1"> &#xe746;</button>
        </div>
        <div class="Spirit">
          <span :class="{active:index === index1}" v-for="(item,index) in img"></span>
        </div>
      </div>
      <div class="Discovery">
        <img src="https://piccdn2.umiwi.com/fe-oss/default/MTYzNTIzNTI3OTIw.png" alt="">
        <div class="Energy" @click="addEnergy">
          登录 | 注册
        </div>
      </div>
    </div>
    <streaming></streaming>
    <course>
      <template #lisi>
        更多 视频课 课程
      </template>
      <template #Flare>
        立即学习
      </template>
      <template #Embrace>
        <i class="iconfont-76c">&#xe76c;</i>
        热门
      </template>
    </course>

  </div>
</template>


<script>
import Bus from "@/utils/EventBus";
import streaming from "@/components/streaming.vue";
import course from "@/components/course.vue";


export default {

  name: 'Navigation',
  components: {
    streaming,
    course,
  },
  data() {
    return {
      // 记录照片的索引
      index1: 0,
      img: [
        'https://piccdn3.umiwi.com/img/202501/06/202501060339045242527382.jpeg',
        'https://piccdn3.umiwi.com/img/202501/22/202501220624359518633947.jpeg',
        'https://piccdn3.umiwi.com/img/202501/06/202501060339045242527382.jpeg',


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
      Forest: false,
      Wonder: true,
    }
  },

  methods: {
    addEnergy() {
      //   发送值给兄弟子组件
      Bus.$emit('Cloud', true)
    },
  }
}

</script>


<style scoped>
@import "../css/Dedaobody.css";

</style>