<template>
  <div>
    <AwokenSkillItem v-for="(item, index) in skills" :item="item" :key="index" />
  </div>
</template>

<script>
// import card from '@/components/card'
import awokenskills from '@/awokenskills'
import AwokenSkillItem from '@/components/AwokenSkillItem'
export default {
  data () {
    return {
      now: (new Date()).toString(),
      skills: awokenskills
    }
  },

  components: {
    AwokenSkillItem
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
    // console.log(awokenskills)
  }
}
</script>

<style>
div {
  font-size: 12px;
}
</style>
