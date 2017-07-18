<template>
  <div id="app">
    <Phone @home="clickHome" :signal="signal" :battery="battery" background="http://ww1.sinaimg.cn/mw690/6ec8ccd0gw1e67grbw0cnj20hs0vk79o.jpg">
      <div class="iphone-page">
        <Application v-for="(item, index) in appList" key="index" class="iphone-app" :name="item.name" :icon="item.icon" />
        <Folder name="音乐"/>
      </div>
    </Phone>
  </div>
</template>

<script>
import Phone from 'vue-phone'
import Application from './components/application'
import Folder from './components/folder'

export default {
  name: 'app',
  data () {
    return {
      signal: 0,
      battery: 100,
      appList: [
        {
          name: 'safari',
          icon: 'http://img.talkandroid.com/uploads/2013/10/facebook_messenger_app_icon.png'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        },
        {
          name: 'safari'
        }
      ]
    }
  },
  components: {
    Phone,
    Application,
    Folder
  },
  methods: {
    clickHome () {
      console.log('home')
    }
  },
  mounted () {
    setInterval(() => {
      this.signal >= 5 ? this.signal = 1 : this.signal++
      this.battery > 0 ? this.battery-- : this.battery = 100
    }, 1000)
  }
}
</script>

<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.iphone-page {
  display: flex;
  flex-wrap: wrap;
  .iphone-app {

  }
}
</style>
