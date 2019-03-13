 <template>
 <div>
   <div class="title">热销推荐</div>
   <ul>
     <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <img class="item-img" :src="item.imgUrl" />
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-buttom">查看详情</button>
      </div>
     </li>
   </ul>
  </div>
</template>

<script>

export default {
  name: 'HomeRecommend',
  data () {
   return{
    recommendList: [{
      id: '0001',
      imgUrl:'http://img1.qunarzz.com/sight/p0/1812/82/820670c947d2eb92a3.img.jpg_200x200_a6c78368.jpg',
      title: '盈香生态园',
      desc: '美丽迷人的生态园'
    },{
      id: '0002',
      imgUrl:'http://img1.qunarzz.com/sight/p0/1603/a9/a9c236b3c1c7835890.img.jpg_200x200_bc63fda6.jpg',
      title: '水乡百花园',
      desc: '梦里水乡的生态园'
    },{
      id: '0003',
      imgUrl:'http://img1.qunarzz.com/sight/p0/1707/85/855e68f1cb85dbc6a3.water.jpg_200x200_73eb26f7.jpg',
      title: '鹭湖半乡温泉',
      desc: '温馨的鹭湖半乡温泉'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .title
    margin-top: .1rem
    line-height:.8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
    .item-title
      ellipsis()
      line-height: .54rem
      font-size: .32rem
    .item-desc
      line-height: .4rem
      color:#d1d1d1
      ellipsis()
    .item-buttom
      line-height: .44rem
      margin-top: .16rem
      background: #ff9300
      padding: 0 .2rem
      border-radius: .06rem
      color: #fff
</style>
