<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl"/>
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
        name: "HomeReconmmend",
        data () {
          return {
            recommendList: [{
              id:'0001',
              imgUrl:'https://img1.qunarzz.com/p/tts9/1807/b4/620b7a0f0932fb02.jpg_r_640x420x90_5afc5d1d.jpg',
              title:'大连生涯海洋世界',
              desc:'浪漫大连首站 浪漫海洋公园'
            },
              {
                id:'0002',
                imgUrl:'https://img1.qunarzz.com/p/tts9/1807/b4/620b7a0f0932fb02.jpg_r_640x420x90_5afc5d1d.jpg',
                title:'大连生涯海洋世界',
                desc:'浪漫大连首站 浪漫海洋公园'
              },{
                id:'0003',
                imgUrl:'https://img1.qunarzz.com/p/tts9/1807/b4/620b7a0f0932fb02.jpg_r_640x420x90_5afc5d1d.jpg',
                title:'大连生涯海洋世界',
                desc:'浪漫大连首站 浪漫海洋公园'
              }]
          }
        }
    }
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow:hidden
    display:flex
    height:1.9rem

    .item-img
      width:1.7rem
      height:1.7rem
      padding: .1rem
    .item-info
      flex:1
      padding: .1rem
      min-width:0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color:#ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background:#ff9300
        padding: 0  .1rem
        border-radius: .06rem
        color:#fff
</style>
