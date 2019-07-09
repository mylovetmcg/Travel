<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="rec of recommendList" :key="rec.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="rec.imgUrl" alt />
        </div>
        <div class="item-info">
          <p class="item-title">{{rec.title}}</p>
          <p class="item-desc">{{rec.desc}}</p>
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
      recommendList: [
        {
          id: "0001",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1707/88/889ae02b07140066a3.img.jpg_200x200_d3b1427c.jpg",
          title: "香港迪士尼乐园香港迪士尼乐园香港迪士尼乐园",
          desc:
            "春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020"
        },
        {
          id: "0002",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1707/88/889ae02b07140066a3.img.jpg_200x200_d3b1427c.jpg",
          title: "香港迪士尼乐园香港迪士尼乐园香港迪士尼乐园",
          desc:
            "春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020"
        },
        {
          id: "0003",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1707/88/889ae02b07140066a3.img.jpg_200x200_d3b1427c.jpg",
          title: "香港迪士尼乐园香港迪士尼乐园香港迪士尼乐园",
          desc:
            "春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020,春晚2日1夜 2020"
        },
        {
          id: "0004",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1707/88/889ae02b07140066a3.img.jpg_200x200_d3b1427c.jpg",
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

.recommend-title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #f2f2f2;
  text-indent: 0.2rem;
}

.item {
  background: #fefefe;
  display: flex;
  // background red
  overflow: hidden;
  height: 1.9rem;

  .item {
    height: 100%;
    width: 100%;
    overflow: hidden;
  }

  .item-img-wrapper {
    width: 1.6rem;
    height: 100%;
    line-height: 1.9rem;
    margin-left: 0.2rem;

    .item-img {
      width: 100%;
    }
  }

  .item-info {
    flex: 1;
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

    .item-button {
      background: #ff9300;
      padding: 0.02rem 0.1rem;
      border-radius: 0.15rem;
      margin-top: 0.1rem;
      font-size: 0.2rem;
      color: #fff;
    }
  }
}
</style>

