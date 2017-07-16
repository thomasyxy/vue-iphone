<template>
  <div class="iphone-application">
    <div class="appliction-icon">
      <img :src="" alt="">
    </div>
  </div>
</template>
<script>
    export default {
      data () {
        return {
          props: {
            name: {
              type: [String],
              default: 'hello'
            },
            icon: {
              type: [String],
              default: ''
            }
          }
        }
      }
    }
</script>
