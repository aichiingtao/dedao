<template>
  <div id="streaming" class="wean">
    <div class="Shadow">
      <h1>免费专区</h1>
      <h4>从免费好课开始，踏上你的得到之旅</h4>
    </div>

    <div class="Harvest">
      <div class="Firefly" v-for="(item,index) in streaming">
        <a href="https://www.baidu.com/">
          <img :src="item.url" alt="">
          <div class="Bounty">
            <div class="Meadow">
              {{ item.title }}
            </div>
            <div class="Current">
              {{ item.title1 }}
            </div>
            <div class="Legacy">
              <i class="iconfont-93a" v-for="index in 5" :key="index">
                &#xe93a;
              </i>
              4.5分
            </div>
            <div class="Cascade">
              {{ item.reserve }}
            </div>

            <!--立即学习-->
            <div class="Flare">
              <a href="#">
                <slot name="Flare1"></slot>
              </a>
            </div>
          </div>

          <!--图标-->
          <div class="Pathway">
            <slot name="Pathway"></slot>
          </div>
        </a>
      </div>
    </div>


  </div>

</template>


<script>

export default {
  name: 'streaming',

  data() {
    return {
      streaming: [
        {
          url: require('@/assets/img_8.png'),
          title: '得到头条',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        },
        {
          url: require('@/assets/img_9.png'),
          title: '文明之旅',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        },
        {
          url: require('@/assets/img_10.png'),
          title: '得到精选',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        },
        {
          url: require('@/assets/img_11.png'),
          title: '脱不花·怎样成为高效学习的人',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        }
      ]
    }
  },
  methods: {
    add(id) {
      this.index1 = id
    }
  }
}

</script>


<style scoped>
@import "@/css/streaming.css";

</style>