<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.url" alt />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeIcons",
  data () {
    return {
      icons: [
        {
          id: "0001",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "景点门票景点门票景点门票"
        },
        {
          id: "0002",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png",
          desc: "珠江夜游"
        },
        {
          id: "0003",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png",
          desc: "水上乐园"
        },
        {
          id: "0004",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "景点门票"
        },
        {
          id: "0005",
          url:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png",
          desc: "自然风光"
        },
        {
          id: "0006",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "景点门票"
        },
        {
          id: "0007",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "景点门票"
        },
        {
          id: "0008",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "景点门票"
        },
        {
          id: "0009",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "景点门票"
        }
      ],
      swiperOption: {
        pagination: ".swiper-pagination"
      }
    };
  },
  computed: {
      pages () {
          const pages = []
          this.icons.forEach((item,index)=>{
              const page = Math.floor(index / 8)
              if(!pages[page]) {
                  pages[page] = []
              }
              pages[page].push(item);
          })
          return pages
      }
  }
};
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl';
@import '~@/assets/styles/mixins.styl';

.icons >>> .swiper-container {
  width: 100%;
  height: 0;
  padding-bottom: 50%;
}

.icons >>> .swiper-pagination {

}

.icon {
  position: relative;
  overflow: hidden;
  width: 25%;
  float: left;
  padding-bottom: 25%;
  background: #fff;
  height: 0;

  .icon-img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0.44rem;
    box-sizing: border-box;
    padding: 0.1rem;

    .icon-img-content {
      height: 100%;
      display: block;
      margin: 0 auto;
    }
  }

  .icon-desc {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    line-height: 0.44rem;
    height: 0.44rem;
    text-align: center;
    color: $darkTextColor;
    ellipsis()
  }
}
</style>
