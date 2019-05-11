<template>
  <div class="wrapper">
    <div class="inner">
      <div class="first-row">
        <div class="icon">
          <img :src="iconSrc">
        </div>
        <div class="name">{{item.skill_name}}</div>
      </div>
      <div class="second-row">{{item.skill_description}}</div>
      <div class="third-row">{{item.skill_description_cn}}</div>
      <div v-if="item.note" class="note-row">
        <div v-html="item.note"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AwokenSkillItem",
  props: ["item"],
  computed: {
    iconSrc() {
      return `data:image/png;base64, ${this.item.skill_image_base64}`;
    }
  }
};
</script>

<style>
.wrapper {
  margin: 10px 0 5px 0;
  padding: 0 10px;
}
.inner {
  border: 1px solid #aaa;
  border-radius: 3px;
}
.first-row {
  display: flex;
  border-bottom: 1px solid #aaa;
}
.icon {
  flex: 0 0 30px;
  box-sizing: border-box;
  padding: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}
img {
  width: 20px;
  height: 20px;
}
.name {
  flex: 1 1 auto;
  display: flex;
  align-items: center;
}
.second-row,
.third-row {
  box-sizing: border-box;
  padding: 5px;
}
.second-row {
  border-bottom: 1px solid #aaa;
}
.note-row {
  border-top: 1px solid #aaa;
  box-sizing: border-box;
  padding: 5px;
}
</style>
