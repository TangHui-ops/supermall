<template>
  <div id="tabbar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  data() {
    //这里存放数据
    return {};
  },
  //监听属性 类似于data概念
  computed: {},
  //监控data中的数据变化
  watch: {},
  //方法集合
  methods: {},
};
</script>
<style>
#tabbar {
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0; 
  right: 0;
  width: 100%;
  height: 50px; 
  /* background-color: #f6f6f6; */
  /* box-shadow: 0 -1px 1px rgba(100, 100, 100, .2); */
}

</style>