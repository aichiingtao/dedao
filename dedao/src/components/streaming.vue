<template>
  <div id="streaming" class="wean">
    <div class="Shadow">
      <h1>精彩直播</h1>
      <h4>直播都用大屏看，沉浸式学习享受</h4>
    </div>
    <div class="Bliss">
      <div class="Mirage" v-for="(item,index) in time">
        <i class="iconfont-8f9">
          &#xe8f9;
        </i>
        {{ item.date }} {{ item.hour }}
      </div>
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
            <div class="Cascade">
              {{ item.reserve }}
            </div>
            <div class="Flare">
              <a href="#">查看直播</a>

            </div>
          </div>
          <div class="Quest">
            直播预告
          </div>
        </a>
      </div>
    </div>

    <div class="Drift">
      <a href="https://www.baidu.com/">
        更多 直播 公开课
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
      time: [
        {date: '02-11', hour: '18:00'},
        {date: '02-12', hour: '18:30'},
        {date: '02-13', hour: '19:00'},
        {date: '02-14', hour: '19:30'},
      ],
      streaming: [
        {
          url: require('@/assets/img.png'),
          title: '从0-1出海东南亚，避开这五大坑',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        },
        {
          url: require('@/assets/img_1.png'),
          title: '从0-1出海东南亚，避开这五大坑',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        },
        {
          url: require('@/assets/img_2.png'),
          title: '从0-1出海东南亚，避开这五大坑',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        },
        {
          url: require('@/assets/img_3.png'),
          title: '从0-1出海东南亚，避开这五大坑',
          title1: '想在东南亚市场开辟商业新版图？千万别错过',
          reserve: '1709人已预约',
        }
      ]
    }
  }
}

</script>


<style scoped>
@import "@/css/streaming.css";

</style>