<template>
    <div class="position">
        <span class="iconfont position__icon">&#xe650;</span>
        <div class="position__content">广东省深圳宝安区西乡街道麻布新村24栋</div>
        <span class="iconfont position__notice">&#xe613;</span>
    </div>
    <div class="search">
        <input type="text" class="search__input iconfont" size="35" placeholder="&#xe606;&nbsp;&nbsp;山姆会员商店优惠商品">
    </div>
    <div class="banner">
        <img src="../assets/banner.jpeg" alt="">
    </div>
    <div class="category">
        <div class="category__item" v-for="(item, index) in category_list" :key="index">
            <img :src="`http://www.dell-lee.com/imgs/vue3/${item.name}.png`" :alt="item.img">
            <span class="desc">{{item.desc}}</span>
        </div>
    </div>
</template>
<script>
export default {
  name: 'StartParts',
  data () {
    return {
      category_list: [
        { name: '超市', desc: '超市便利' },
        { name: '菜市场', desc: '菜市场' },
        { name: '水果店', desc: '水果店' },
        { name: '鲜花', desc: '鲜花绿植' },
        { name: '医药健康', desc: '医药健康' },
        { name: '家居', desc: '家居时尚' },
        { name: '蛋糕', desc: '烘培蛋糕' },
        { name: '签到', desc: '签到' },
        { name: '大牌免运', desc: '大牌免运' },
        { name: '红包', desc: '红包套餐' }
      ]
    }
  }
}
</script>
<style lang="scss">

// @import '../css/mixin.scss';
@import '../css/index.scss';
.position{
    padding: .18rem .18rem 0;
    @include ellipsis;
    font-size:.16rem;
    &__icon{
        font-size: .18rem;
    }
    &__content{
        display: inline;
    }
    &__notice{
        font-size: .18rem;
        position: absolute;
        right:.1rem;
    }
}
.search{
    box-sizing: border-box;
    width: 100%;
    padding: 0 .18rem;
    margin-top:.2rem;
    border-radius: 25%;
    &__input{
        box-sizing: border-box;
        font-size: .14rem;
        padding:.05rem;
        width:100%;
        background-color: #f5f5f5;
        border-radius: .16rem;
    }
}
.banner{
    box-sizing: border-box;
    width: 100%;
    padding: .18rem;
    img{
        width: 100%;
    }
}
.category{
    box-sizing: border-box;
    width: 100%;
    padding: .18rem;
    // background: red;
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
    border-bottom: .15rem solid #f5f5f5;
    &__item{
        box-sizing: border-box;
        width: .6rem;
        height: .6rem;
        // background-color: orange;
        // border: 1px solid black;
        margin-bottom: .1rem;
        display: flex;
        flex-direction: column;
        justify-content: center;

        img{
            margin: 0 auto;
            width: 75%;
            border-radius: 50%;
        }
        .desc{
            text-align: center;
            margin-top:.1rem;
        }
    }
}
</style>
