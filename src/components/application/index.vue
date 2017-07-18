<template>
  <div class="iphone-application">
    <div class="appliction-icon">
      <img :src="icon" alt="">
    </div>
    <div class="application-name">
      {{name}}
    </div>
  </div>
</template>
<script>
import defaultIcon from './default_icon.png'
export default {
  name: 'application',
  data () {
    return {
    }
  },
  props: {
    name: {
      type: [String],
      default: 'hello'
    },
    icon: {
      type: [String],
      default: defaultIcon
    }
  }
}
</script>
<style lang="less" scoped>
  .iphone-application {
    box-sizing: border-box;
    width: 25%;
    padding: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
  .appliction-icon {
    width: 70px;
    height: 70px;
    display: flex;
    img {
      width: 100%;
    }
  }
  .application-name {
    color: #fff;
  }
</style>
