<template>
  <div class="iphone-application">
    <div class="appliction-icon">
      <img :src="icon" alt="">
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
