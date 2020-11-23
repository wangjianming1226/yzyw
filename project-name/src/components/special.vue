<template>
  <div class="special">
    <div class="title">{{ title }}</div>
    <div class="special_flex">
      <div
        v-for="(value, index) in dataImg"
        v-bind:key="value"
        :style="conTop[index]"
      >
        <!-- <img :src="dataImg[index]"> -->
      </div>
    </div>
  </div>
</template>
<script>
import a from "../assets/a.jpg";
import b from "../assets/b.jpg";
import c from "../assets/c.jpg";
// import d from '../assets/d.jpg'
// import e from '../assets/e.jpg'
export default {
  name: "Special",
  data: function () {
    return {
      title: "专题",
      dataImg: [a, b, c],
      dataContent: ["人才峰会", "BIM专题", "造价专题", "总咨询师", "企业管理"],
      ImgIndex: 0,
      //背景图片
      conTop: [
        {
          backgroundImage: "url(" + a + ")",
          backgroundRepeat: "no-repeat",
          //响应式
          backgroundSize: "cover",
        },
        {
          backgroundImage: "url(" + b + ")",
          backgroundRepeat: "no-repeat",
          backgroundSize: "cover",
        },
        {
          backgroundImage: "url(" + c + ")",
          backgroundRepeat: "no-repeat",
          backgroundSize: "cover",
        },
      ],
    };
  },
};
</script>
<style scoped>
.special {
  height: 740px;
  background: #f6f6f6;
}
.title {
  display: flex;
  width: 100%;
  padding-top: 50px;
  justify-content: center;
  font-size: 25px;
}
.special_flex {
  display: flex;
  width: 100%;
  overflow: hidden;
  margin-top: 50px;
}
.special_flex div {
  flex: 1;
  width: 33%;
  height: 500px;
  border: 1px solid white;
}
.special_flex img {
  width: 100%;
}
</style>