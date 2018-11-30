<template>
    <div class="icons">
      <swiper>
        <swiper-slide v-for="(page,index) of pages" :key="index">
          <div class="icon" v-for="item of page" :key="item.id">
            <div class="icon-img">
              <img class='icon-img-content' :src="item.imgUrl"/>
            </div>
            <p class="icon-desc">{{item.desc}}</p>
          </div>
        </swiper-slide>

        </swiper>


    </div>

</template>

<script>
    export default {
        name: "HomeIcons",
        data() {
          return{
            iconList:[{
              id:'0001',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542733008190&di=0c57070a1b8863fc24900264f7fa5d83&imgtype=0&src=http%3A%2F%2Fwww.sj520.cn%2Fsc%2Fima%2F20160901150330_72791.jpg',
              desc:'景点门票'
            },{
              id:'0002',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542735095517&di=7c932ef130b27290df958025c38af298&imgtype=0&src=http%3A%2F%2Fp5.zbjimg.com%2Ftask%2F2011-09%2F10%2F1043889%2Flarge4e6b2a52069ff.jpg',
              desc:'滑雪季节'
            },{
              id:'0003',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542735195123&di=89f2c1a92452e829754ac2eea0f313a5&imgtype=0&src=http%3A%2F%2Fh1.syoits.com%3A8680%2FUploads%2FTheme%2F1509685680.jpg',
              desc:'泡温泉'
            },{
              id:'0004',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542735290203&di=3a64627c4d40dae350ce40367c5b1445&imgtype=jpg&src=http%3A%2F%2Fimg4.imgtn.bdimg.com%2Fit%2Fu%3D2940205784%2C3664941886%26fm%3D214%26gp%3D0.jpg',
              desc:'动物园'
            },{
              id:'0005',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542735290203&di=3a64627c4d40dae350ce40367c5b1445&imgtype=jpg&src=http%3A%2F%2Fimg4.imgtn.bdimg.com%2Fit%2Fu%3D2940205784%2C3664941886%26fm%3D214%26gp%3D0.jpg',
              desc:'动物园'
            },{
              id:'0006',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542735290203&di=3a64627c4d40dae350ce40367c5b1445&imgtype=jpg&src=http%3A%2F%2Fimg4.imgtn.bdimg.com%2Fit%2Fu%3D2940205784%2C3664941886%26fm%3D214%26gp%3D0.jpg',
              desc:'动物园'
            },{
              id:'0007',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542735290203&di=3a64627c4d40dae350ce40367c5b1445&imgtype=jpg&src=http%3A%2F%2Fimg4.imgtn.bdimg.com%2Fit%2Fu%3D2940205784%2C3664941886%26fm%3D214%26gp%3D0.jpg',
              desc:'动物园'
            },{
              id:'0008',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1542735290203&di=3a64627c4d40dae350ce40367c5b1445&imgtype=jpg&src=http%3A%2F%2Fimg4.imgtn.bdimg.com%2Fit%2Fu%3D2940205784%2C3664941886%26fm%3D214%26gp%3D0.jpg',
              desc:'动物园'
            },]
          }
        },
      computed:{
          pages (){
            const pages = []
            this.iconList.forEach((item,index) =>{
              const page = Math.floor(index/8)
              if(!pages[page]){
                pages[page]=[]
              }
              pages[page].push(item)
            })
            return pages
          }
      }
    }
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons>>>.swiper-container

    height:0
    padding-bottom:50%
  .icons
    margin-top: .1rem
    .icon
      position:relative
      overflow:hidden
      float:left
      width:25%
      height:0
      padding-bottom:25%

      .icon-img
        position:absolute
        top:0
        left:0
        right:0
        bottom: .44rem
        box-sizing:border-box
        padding: .1rem
        .icon-img-content
          display:block
          margin:0 auto
          height:100%
      .icon-desc
        position:absolute

        left:0
        right:0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align:center
        color:$darkTextColor
        ellipsis()


</style>
