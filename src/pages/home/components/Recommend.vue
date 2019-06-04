<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of  recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  data() {
    return {
      recommendList: [{
        id:'001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/57/579b6c97900745db.water.jpg_200x200_f09770c8.jpg',
        title: '橘子洲',
        desc: '橘子洲是个好地方',

      },{
        id:'002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1905/29/296e5659470d69bea3.img.jpg_200x200_75593f9f.jpg',
        title: '世界之窗',
        desc: '世界之窗是个好地方',

      },{
        id:'003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/b7aa220089fa8054e6e012bafff63042.jpg_200x200_650160bf.jpg',
        title: '长沙生态动物园',
        desc: '长沙生态动物园是个好地方',

      }]
    }
  },
};
</script>

<style lang="stylus" scoped>
@improt '~styles/mixins.styl'
.title 
  margin-top: .2rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem


.item 
  overflow: hidden //内容溢出元素框时发生的事情:内容会被修剪，并且其余内容是不可见的。
  display: flex
  height: 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex 1      
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-button
      line-height .44rem
      margin-top .16rem
      background #ff9300
      padding 0 .2rem
      border-radius .06rem
      color #fff
</style>

