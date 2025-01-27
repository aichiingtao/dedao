<template>
  <div id="app">
      <ul class="Compass">
        <li v-for="(item,index) in list" :class="{active: index === index1}"
            @click="Destiny(index)" v-show="Bloom">
          {{item}}
        </li>
      </ul>
    <DedaoHead></DedaoHead>
    <Dedaobody></Dedaobody>



  </div>
</template>

<script>
import DedaoHead from './components/DedaoHead.vue'
import Dedaobody from './components/Dedaobody.vue'
import streaming from './components/streaming.vue'


export default {
  name: 'App',
  components: {
    DedaoHead,
    Dedaobody,
    streaming,
  },

  data(){
    return{
      // 储存页面滚动了多少
      scrollPosition: 0,
      // 储存盒子滚动了多少距离
      distance: 0,
      index1:0,
      list:['直播','课程','免费专区','得到听书','电子书','得到新商学'],
      Bloom:false,
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll); // 监听滚动事件
    window.addEventListener('scroll', this.updateDistance); // 监听某个元素与顶部的距离
    this.updateDistance(); // 初始化距离
  },
  methods:{
    Destiny(id){
      this.index1 = id
    },
    handleScroll(){
      console.log(this.scrollPosition)
      this.scrollPosition = window.scrollY;

      if (this.scrollPosition >= 450){
        this.Bloom = true
      }
      else {
        this.Bloom = false
      }
    },
    updateDistance(){
      const box = this.$refs.targetBox;

    },

  }
}
</script>



<style>
@import './css/initialization.css';
.wean{
  width: 1200px;
  margin: 0 auto;
}
.Compass{
  position: fixed;
  top: 50%;
  transform: translateY(-50%);
  right: 10px;
  padding: 10px 0;
  background-color: #f9f9f9;
  border: 1px solid lightgray;
  border-radius: 8px;
  li{
    cursor: pointer;
    height: 32px;
    padding: 0 5px;
    font-size: 12px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #333333;

    &:hover{
      background-color: #ffffff;
      color: #ff6b00;
    }
  }
  .active{
    background-color: #ffffff;
    color: #ff6b00;
  }
}
</style>
