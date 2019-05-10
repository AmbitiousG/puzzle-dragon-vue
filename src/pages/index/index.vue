<template>
  <div>
    <div>武汉的小伙伴们晚上好!</div>
    <div>{{now}}</div>
  </div>
</template>

<script>
// import card from '@/components/card'

export default {
  data () {
    return {
      now: (new Date()).toString()
    }
  },

  components: {
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
div {
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
