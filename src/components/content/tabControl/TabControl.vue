<template>
  <div class="tab-control">
      <div v-for="(item, index) in titles" :key="index" :class="{active:index === currentIndex}" 
          class="tab-control-item" @click="itemClick(index)">
          <span>{{item}}</span>
      </div>
  </div>
</template>

<script>
//例如：import 《组件名称》 from '《组件路径》';
export default {
  name: "TabControl",
  props: {
    titles: {
      type: Array,
      default() {
        return []
      },
    },
  },
  data() {
      return {
          currentIndex: 0
      }
  },
  methods:{
      itemClick(index){
          this.currentIndex = index;
          this.$emit('tabClick', index)
      }
  }
};
</script>
<style>
/* @import url(); 引入公共css类 */
.tab-control{
    display: flex;
    text-align: center;
    background-color: #ffffff;
    height: 40px;
    line-height: 40px;
}
.tab-control-item{
    flex: 1;
}
.tab-control-item span{
    padding: 5px;
}
.active{
    color: var(--color-high-text);
}
.active span{
    border-bottom: 2px solid var(--color-tint);
}
</style>