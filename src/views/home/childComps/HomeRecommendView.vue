<template>
    <div class="recommends">
        <div v-for="(item,index) in recommends" :key="index" class="recommends-item">
            <a :href="item.link">
                <img :src="item.image" alt=""/>
                <div>{{item.title}}</div>
            </a>
        </div>
    </div>
</template>

<script>
//例如：import 《组件名称》 from '《组件路径》';
export default {
    name: 'HomeRecommendView',
    props:{
        recommends:{
            type: Array,
            default(){
                return []
            }
        }
    },
   data() {
      //这里存放数据
      return {
      };
   }
}
</script>
<style>
   /* @import url(); 引入公共css类 */
   .recommends{
       display: flex;
       width: 100%;
       text-align: center;
       font-size: 12px;
       padding: 10px 0 20px;
       border-bottom: 10px #eeeeee solid;
   }
   .recommends-item{
       flex: 1;
   }
   .recommends-item img{
       width: 70px;
       height: 70px;
       margin-bottom: 10px;
   }
</style>