<template>
<div>
    <div class="recommend">
    <div class="recommend-title">
        <img class="recommend-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">
        猜你喜欢
    </div>
    <ul>
        <router-link tag="li"
         class="item border-bottom"
         v-for="item in list"
         :key="item.id"
         :to="'/detail/' + item.id"
         >
                <img class="item-img" :src="item.imgUrl">
                <div class="item-img-tag" style="background-image:url(https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png)">随买随用</div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">
                    <span class="iconfont">&#xe62b;&#xe62b;&#xe62b;&#xe62b;&#xe62b;</span>
                    <span class="comment">{{item.comment}}条评论</span>
                </p>
                <div class="price">
                    <span class="flag">¥</span>
                    {{item.price}}
                    <span class="qi">起</span>
                    <span class="position">{{item.position}}</span>
                </div>
            </div>
        </router-link>
    </ul>
    </div>
</div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  },
  data () {
    return {

    }
  }
}
</script>

<style lang="stylus" scoped>
.recommend-title
  box-sizing border-box
  padding-left .4rem
  padding-top .3rem
  background-color #fff
  font-size 0.36rem
  flex 1
  height 1rem
.recommend-title-img
  width 5%
//   每一条图文的样式
ul
  width 100%
  background-color #fff
ul li
  display flex
  flex 1
  background #fff
  height 2.4rem
  padding-top .2rem
  padding-bottom .2rem
  box-sizing border-box
  margin-left .2rem
.item-info .item-title
    font-size .35rem
.item-img
    height 2rem
    height 2rem
.item-img-tag
    position: absolute
    background-size: 100%
    color: #fff
    font-size: .2rem
    line-height: .38rem
    text-indent: .04rem
.item-info
    padding-top .2rem
    flex 1
    padding-left .3rem
.item-desc
    padding-top .2rem
.item-info .item-desc .iconfont
    width 100%
    display inline
    padding-top .2rem
    font-size .2rem
    color #ffb436
    letter-spacing 0.02rem
.item-desc .comment
    display inline
    padding-left .3rem
    color #616161
    // 每一条的价钱和位置
.item-info .price
    font-size .4rem
    padding-top .4rem
.item .price,
.item .price .flag
    color #ff8300
.item .price .flag
    font-size .3rem
.item .price .qi
    font-size .2rem
    color #616161
.item .price .position
    padding-top .15rem
    padding-right .4rem
    font-size .2rem
    color #616161
    float right

</style>
