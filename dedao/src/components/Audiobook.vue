<template>
  <div id="streaming" class="wean">
    <div class="Shadow">
      <h1>得到听书</h1>
      <h4>
        已有3400+本听书随你挑选，另外每天还会上新1本，跟上你的学习速度。我们会珍惜你每分钟的阅读时间，给你专业的好书解读。</h4>
    </div>
    <div class="Glimmer">
      <ul class="Flourish">
        <li @click="add(index,item)" v-for="(item,index) in time" :class="{active: index === index1}">
          {{ item }}
        </li>
      </ul>
      <div class="iconfont-741">
        &#xe741;
      </div>
      <div class="iconfont-746">
        &#xe746;
      </div>
    </div>

    <div class="Harvest" v-for="(category,index) in streaming" :key="index" v-show="Solstice === category.title2">
      <div class="Firefly" v-for="(item,itemIndex) in category.Wonder" :key="itemIndex">
        <a href="https://www.baidu.com/">
          <img :src="item.url" alt="" class="Clarity">
          <div class="Bounty">
            <div class="Meadow">
              {{ item.title }}streaming.
            </div>
            <div class="Legacy1">
              <i class="iconfont-93a" v-for="index in 5" :key="index">
                &#xe93a;
              </i>
              4.5分
            </div>
            <div class="Cascade">
              {{ item.reserve }}
            </div>
            <i class="iconfont-6ff">&#xe6ff;</i>
          </div>
        </a>
      </div>
    </div>

    <!-- 底部更多-->
    <div class="Drift">
      <a href="https://www.baidu.com/">
        <slot name="lisi1"></slot>
      </a>

      <i class="iconfont-746">&#xe746;</i>
    </div>

  </div>

</template>


<script>

export default {
  name: 'streaming',

  data() {
    return {
      Solstice: '热门',
      index1: 0,
      time: ['热门', '名家讲书', '精品听书'],
      streaming: [
        {
          title2: '热门',
          Wonder: [
            {
              url: require('@/assets/img_12.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '3.1万次学习',
            },
            {
              url: require('@/assets/img_12.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '3.1万次学习',
            },
          ]

        },
        {
          title2: '名家讲书',
          Wonder: [
            {
              url: require('@/assets/img_12.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '3.1万次学习',
            },
            {
              url: require('@/assets/img_12.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '3.1万次学习',
            },
            {
              url: require('@/assets/img_12.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '3.1万次学习',
            },
          ]
        },
        {
          title2: '精品听书',
          Wonder: [{
            url: require('@/assets/img_12.png'),
            title: '从0-1出海东南亚，避开这五大坑',
            title1: '想在东南亚市场开辟商业新版图？千万别错过',
            reserve: '3.1万次学习',
          }]
        },
      ]
    }
  },
  methods: {
    add(id,item) {
      this.index1 = id
      this.Solstice = item

    }
  }
}

</script>


<style scoped>
@import "@/css/streaming.css";

</style>