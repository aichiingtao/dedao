<template>
  <div id="streaming" class="wean">
    <div class="Shadow">
      <h1>精选课程</h1>
      <h4>覆盖20+领域，随时随地终身可学</h4>
    </div>
    <div class="Glimmer">
      <ul class="Flourish">
        <li @click="addtab(index,item)" v-for="(item,index) in time"
            :class="{active: index === index1}"
        >
          {{ item }}
        </li>
      </ul>
      <div class="iconfont-741" v-show="isshow" >
        &#xe741;
      </div>
      <div class="iconfont-746" >
        &#xe746;
      </div>
    </div>

    <div class="Harvest" v-for="(category) in streaming ">
      <div class="Firefly" v-for="(item) in category.Flourish" v-show="tabtilie === category.title2">
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


            <div class="Flare">
              <a href="#">
                <slot name="Flare"></slot>
              </a>
            </div>
          </div>
          <div class="Embrace">
            <slot name="Embrace"></slot>
          </div>
        </a>
      </div>
    </div>

    <!-- 底部更多-->
    <div class="Drift">
      <a href="https://www.baidu.com/">
        <slot name="lisi"></slot>
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
      tabWidth: 100,
      currentTabIndex: 0,
      isshow:false,
      tabtilie:'视频课',
      index1: 0,
      time: ['视频课', '视自我提升', '金融学', '商业', '心理学', '历史', '文学', '视频课', '职场', '职场', '职场', '职场', '职场', '职场','职场','职场','职场','职场',],
      streaming: [
        {
          title2: '视频课',
          Flourish: [{
            url: require('@/assets/img_4.png'),
            title: '从0-1出海东南亚，避开这五大坑',
            title1: '想在东南亚市场开辟商业新版图？千万别错过',
            reserve: '1709人已预约',
          },
            {
              url: require('@/assets/img_4.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_4.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },{
              url: require('@/assets/img_4.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            }
          ]
        },
        {
          title2: '视自我提升',
          Flourish: [{
            url: require('@/assets/img_5.png'),
            title: '从0-1出海东南亚，避开这五大坑',
            title1: '想在东南亚市场开辟商业新版图？千万别错过',
            reserve: '1709人已预约',
          },
            {
              url: require('@/assets/img_5.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_5.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_5.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },]

        },
        {
          title2: '金融学',
          Flourish:[ {
            url: require('@/assets/img_6.png'),
            title: '从0-1出海东南亚，避开这五大坑',
            title1: '想在东南亚市场开辟商业新版图？千万别错过',
            reserve: '1709人已预约',
          },
            {
              url: require('@/assets/img_6.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_6.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_6.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },]

        },
        {
          title2: '商业',
          Flourish: [
            {
              url: require('@/assets/img_7.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_7.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_7.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
            {
              url: require('@/assets/img_7.png'),
              title: '从0-1出海东南亚，避开这五大坑',
              title1: '想在东南亚市场开辟商业新版图？千万别错过',
              reserve: '1709人已预约',
            },
          ]

        }
      ]
    }
  },

  methods: {
    addtab(id, item) {
      this.index1 = id
      this.tabtilie = item
    },
  }
}

</script>


<style scoped>
@import "@/css/streaming.css";

</style>