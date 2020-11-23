<template>
  <div class="banner">
    <div class="item">
      <img :src="dataList[currentIndex]" />
    </div>
    <div class="page">
      <ul>
        <li @click="gotoPage(prevIndex)">&lt;</li>
        <li v-for="(item,index) in dataList" v-bind:key="item" @click="gotoPage(index)" :class="{ current: currentIndex == index }"> {{ index + 1 }} </li>
        <li @click="gotoPage(nextIndex)">&gt;</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Jdt",
  data: function () {
    return {
      //图片地址
      dataList: [
        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1603514224381&di=83fb1611cf8a976410b2c244b5f29c4a&imgtype=0&src=http%3A%2F%2Fimg.pconline.com.cn%2Fimages%2Fupload%2Fupc%2Ftx%2Fwallpaper%2F1208%2F24%2Fc2%2F13179846_1345796441969.jpg",
        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1603514224380&di=f9697db2ac3aca0bd539a8b6c696a90f&imgtype=0&src=http%3A%2F%2Fimg.pconline.com.cn%2Fimages%2Fupload%2Fupc%2Ftx%2Fwallpaper%2F1205%2F22%2Fc0%2F11704482_1337657341929.jpg",
        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1603514224380&di=af55ea77db57847d68e1aeeebb03806c&imgtype=0&src=http%3A%2F%2Fpic1.win4000.com%2Fwallpaper%2F2017-11-24%2F5a17812a08ef0.jpg",
      ],
      //显示的图片
      currentIndex: 0,
      timer: null, //定时器
    };
  },
  methods: {
    gotoPage(index) {
      this.currentIndex = index;
    },
    //定时器
     runInv() {
      this.timer = setInterval(() => {
        this.gotoPage(this.nextIndex);
      }, 1000);
    }
  },
  computed: {
    //上一张
    prevIndex() {
      if (this.currentIndex == 0) {
        return this.dataList.length - 1;
      } else {
        return this.currentIndex - 1;
      }
    },
    //下一张
    nextIndex() {
      if (this.currentIndex == this.dataList.length - 1) {
        return 0;
      } else {
        return this.currentIndex + 1;
      }
    },
  },
  
};

</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
}
ul li {
  list-style: none;
  float: left;
  width: 30px;
  height: 40px;
  text-align: center;
  cursor: pointer;
  color: rgba(255, 255, 255, 0.8);
  font-size: 14px;
}
.banner {
  width: 100%;
  position: relative;
}
.banner img {
  width: 100%;
  display: block;
}
.banner .page {
  background: rgba(0, 0, 0, 0.5);
  position: absolute;
  right: 0;
  bottom: 0;
  width: 100%;
}
.banner .page ul {
  float: right;
}
.current {
  color: #ff6700;
}
</style>