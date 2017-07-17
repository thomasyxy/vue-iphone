<template>
  <div class="iphone-folder">
    <div class="folder-name">
      {{name}}
    </div>
  </div>
</template>
<script>
export default {
  name: 'folder',
  data () {
    return {
    }
  },
  props: {
    name: {
      type: [String],
      default: '文件夹'
    }
  }
}
</script>
<style lang="less">
</style>
