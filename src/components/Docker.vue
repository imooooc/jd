<template>
  <div class="docker">
    <div class="docker__tab" v-for="(tab, index) in tabList" :key=index >
      <div class="docker__tab__icon  iconfont" v-html="tab.icon"></div>
      <div class="docker__tab__text">{{tab.text}}</div>
    </div>
  </div>
  <!-- <router-view/> -->
</template>
<script>
export default {
  name: 'App',
  data () {
    return {
      tabList: [{
        text: '首页',
        icon: '&#xe661;'
      }, {
        text: '购物车',
        icon: '&#xe638;'
      }, {
        text: '订单',
        icon: '&#xe713;'
      }, {
        text: '我的',
        icon: '&#xe641;'
      }
      ]
    }
  }
}
</script>
<style lang="scss">
@import '../css/index.scss';
*{
    margin:0;
  padding:0;
}

.docker{
  background-color: #f5f5f5;
  display: flex;
  flex-direction: row;
  position: fixed;
  bottom: 0;

  left:0;
  width: 100%;
  &__tab{
    // background-color: blue;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    font-size:14px;
    width:25%;
    height: 50px;
    text-align: center;
    // border: 1px solid red;
    &__icon{
      color: tomato;
      font-size: 22px;
    }
    &__text{
      color:black;
    }
  }
}
</style>
