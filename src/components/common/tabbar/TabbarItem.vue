<template>
<!-- 所有的item都展示同一个图片，同一个文字 -->
  <div class="tabbar_item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>
    <!-- <i class="iconfont icon-shouye2"></i>
    <div>我的</div>-->
  </div>
</template>

<script>
//例如：import 《组件名称》 from '《组件路径》';
export default {
  props: {
    path: String,
    activeColor:{
        type: String,
        default: 'red'
    }
  },
  data() {
    //这里存放数据
    return {
      //   isActive: false,
    };
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !== -1;
    },
    activeStyle(){
        return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    itemClick() {
      this.$router.replace(this.path);
    },
  },
};
</script>
<style>
.tabbar_item {
  flex: 1;
  background: #f6f6f6;
  box-shadow: 0 -3px 1px rgba(100, 100, 100, 0.2);
  height: 50px;
  text-align: center;
}
.iconfont {
  font-size: 24px;
  margin-top: 17px;
  margin-bottom: 5px;
  vertical-align: middle;
}
</style>