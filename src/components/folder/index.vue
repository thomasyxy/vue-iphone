<template>
  <div class="iphone-folder">
    <div class="folder-collection">
      <div class="folder-application" v-for="app in apps">
        <div class="folder-application-icon">
          
        </div>
        <div class="folder-application-name">

        </div>
      </div>
    </div>
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
    },
    apps: {
      type: [Array],
      default: []
    }
  }
}
</script>
<style lang="less" scoped>
.iphone-folder {
  box-sizing: border-box;
  width: 25%;
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.folder-collection {
  width: 100%;
  width: 70px;
  height: 70px;
  border-radius: 10px;
  background: rgba(255, 255, 255, 0.2);
}
.folder-name {
  color: #fff;
}
</style>
