<template>
    <div class="goods">
        <goods-list-item v-for="(item,index) in goods" :key="index"
             :goods-item="item"/>
    </div>
</template>

<script>
import GoodsListItem from './GoodsListItem'
export default {
    name: 'GoodsList',
    props:{
        goods:{
            type:Array,
            default(){
                return []
            }
        }
    },
   data() {
      //这里存放数据
      return {
      };
   },
   components: {
       GoodsListItem
   },
}
</script>
<style>
   /* @import url(); 引入公共css类 */
   .goods{
       display: flex;
       flex-wrap: nowrap;
       justify-content: space-around;
       padding: 3px;
   }

</style>