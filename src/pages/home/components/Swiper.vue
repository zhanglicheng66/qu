<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>


    </swiper>
  </div>
</template>

<script>
    export default {
        name: "HomeSwiper",
        data(){
          return{
            swiperOption: {
              pagination:'.swiper-pagination',
              loop:true
            },
            swiperList:[{
              id:'0001',
              imgUrl:"https://aecpm.alicdn.com/simba/img/TB14ab1KpXXXXclXFXXSutbFXXX.jpg_q50.jpg"
            },{
              id:'0002',
              imgUrl:"https://aecpm.alicdn.com/simba/img/TB1CWf9KpXXXXbuXpXXSutbFXXX.jpg_q50.jpg"
            }]
          }
        }
    }
</script>

<style lang="stylus" scoped>
  .wrapper >>>.swiper-pagination-bullet-active
    background:#fff !important
  .wrapper
    overflow:hidden
    width: 100%
    height:0
    padding-bottom:31.25%
    background: #333333
    .swiper-img
      width:100%
</style>
