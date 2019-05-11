<template>
  <div class="home-wrapper">
    <div class="img-wrapper">
      <img src="/static/images/icon.png" alt="">
    </div>
    <div class="search-wrapper">
      <a open-type="switchTab" href="../../pages/awokenSkills/main" class="navigate">查看潜在觉醒</a>
    </div>
  </div>
</template>

<script>
// import card from '@/components/card'
export default {
  data () {
    return {
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
    // console.log(awokenskills)
  }
}
</script>

<style>
page {
  height: 100%;
}
div {
  font-size: 12px;
}
.home-wrapper {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.img-wrapper,
.img-wrapper image {
  width: 64px;
  height: 64px;
}
.search-wrapper {
  margin-top: 10px;
  border-width: 1px 0;
  border-color: #aaa;
  border-style: solid;
  width: 100%;
}
.navigate {
  color: #3a9be7;
  padding: 10px 20px;
  box-sizing: border-box;
}
</style>
