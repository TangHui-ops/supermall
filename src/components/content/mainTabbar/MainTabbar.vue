<template>
  <div>
    <Tabbar>
      <TabbarItem path="/home" activeColor="red">
        <svg slot="item-icon" class="icon" aria-hidden="true">
          <use xlink:href="#icon-shouye"></use>
        </svg>
        <svg slot="item-icon-active" class="icon" aria-hidden="true">
          <use xlink:href="#icon-shouye-copy" />
        </svg>
        <div slot="item-text">首页</div>
      </TabbarItem>
      <TabbarItem path="/category" activeColor="red">
        <svg slot="item-icon" class="icon" aria-hidden="true">
          <use xlink:href="#icon-icon"></use>
        </svg>
        <svg slot="item-icon-active" class="icon" aria-hidden="true">
          <use xlink:href="#icon-icon-copy" />
        </svg>
        <div slot="item-text">分类</div>
      </TabbarItem>
      <TabbarItem path="/cart" activeColor="red">
        <svg slot="item-icon" class="icon" aria-hidden="true">
          <use xlink:href="#icon-shouye1"></use>
        </svg>
        <svg slot="item-icon-active" class="icon" aria-hidden="true">
          <use xlink:href="#icon-shouye1-copy-copy" />
        </svg>
        <div slot="item-text">购物车</div>
      </TabbarItem>
      <TabbarItem path="/profile" activeColor="red">
        <svg slot="item-icon" class="icon" aria-hidden="true">
          <use xlink:href="#icon-shouye2"></use>
        </svg>
        <svg slot="item-icon-active" class="icon" aria-hidden="true">
          <use xlink:href="#icon-shouye2-copy" />
        </svg>
        <div slot="item-text">我的</div>
      </TabbarItem>
    </Tabbar>
  </div>
</template>

<script>
import Tabbar from "components/common/tabbar/Tabbar";
import TabbarItem from "components/common/tabbar/TabbarItem";
import icon from "assets/foot/iconfont.js";

export default {
  data() {
    //这里存放数据
    return {};
  },
  components: {
    Tabbar,
    TabbarItem,
  },
};
</script>
<style lang="scss">
// @import "./assets/foot/iconfont.css";

.icon {
  width: 1em;
  height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
  font-size: 24px;
}
</style>