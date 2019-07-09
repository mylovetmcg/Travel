<template>
  <div>
    <div class="weekend-title">爽玩周末</div>
    <ul>
      <li class="item border-bottom" v-for="rec of weekendList" :key="rec.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="rec.imgUrl" alt />
        </div>
        <div class="item-info">
          <p class="item-title">{{rec.title}}</p>
          <p class="item-desc">{{rec.desc}}</p>
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
      weekendList: [
        {
          id: "0001",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg",
          title: "香港迪士尼乐园香港迪士尼乐园香港迪士尼乐园",
          desc:
            "春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020"
        },
        {
          id: "0002",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg",
          title: "香港迪士尼乐园香港迪士尼乐园香港迪士尼乐园",
          desc:
            "春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020"
        },
        {
          id: "0003",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg",
          title: "香港迪士尼乐园香港迪士尼乐园香港迪士尼乐园",
          desc:
            "春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020"
        },
        {
          id: "0004",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg",
          title: "香港迪士尼乐园香港迪士尼乐园香港迪士尼乐园",
          desc:
            "春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/mixins.styl';

.weekend-title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #f2f2f2;
  text-indent: 0.2rem;
}

.item {
  background: #fefefe;
  overflow: hidden;
//   height: 3.5rem;

  .item-img-wrapper {
    width: 100%;
    // height: 2rem

    .item-img {
      width: 100%;
    }
  }

  .item-info {
    padding: 0.15rem;
    overflow: hidden;

    .item-title {
      line-height: 0.5rem;
      font-size: 0.32rem;
      ellipsis();
    }

    .item-desc {
      line-height: 0.38rem;
      height: 0.38rem;
      font-size: 0.2rem;
      color: #bbb;
      ellipsis();
    }
  }
}
</style>