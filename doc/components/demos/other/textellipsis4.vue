<style lang="less">
.textellipsis-demo4 {
  .h-text-ellipsis-limit-text {
    white-space: pre-wrap;
  }
}
</style>

<template>
  <TextEllipsis class="textellipsis-demo4" :text="text" :height="100" v-width="200" :isLimitHeight="isLimitHeight">
    <span slot="before" class="h-tag h-tag-red">new</span>
    <template slot="more"><span>...</span><span class="link" @click="isLimitHeight=false">查看更多</span></template>
    <span slot="after" class="link" v-if="!isLimitHeight" @click="isLimitHeight=true">收起</span>
  </TextEllipsis>
</template>

<script>

export default {
  data() {
    return {
      text: '《华盛顿自由灯塔报》几天前报道称，\n美国国防部官员透露中国近日进行第十次东风-41洲际导弹的试射活动，这次试射中东风-41导弹投射了多个弹头并成功命中中国西部靶场目标。',
      isLimitHeight: true
    };
  },
  methods: {
  }
};
</script>
