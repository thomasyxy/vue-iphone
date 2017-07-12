<template>
  <div class="iphone-application">
    <div class="appliction-icon">
      {{name}}
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
            }
          }
        }
      }
    }
</script>
