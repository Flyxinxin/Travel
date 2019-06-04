<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of  recommendList" :key="item.id">
          <div class="item-img-wraper">
          <img class="item-img" :src="item.imgUrl">
          </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeWeekend",
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
.item-img-wraper
  overflow hidden
  height 0
  padding-bottom 33.9%
  .item-img
    width 100%
.item-info    
padding .1rem
.item-title
    line-height .54rem
    font-size .32rem
    ellipsis()
.item-desc
    line-height .4rem
    color #ccc
    ellipsis()
</style>

