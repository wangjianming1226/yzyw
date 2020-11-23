<template>
  <div class="header">
    <div class="left-logo">
      <img src="../assets/yizhuanyiwalogo.png" alt="" />
    </div>
    <div class="right-nav">
      <el-menu
        :default-active="activeIndex"
        class="el-menu-demo"
        mode="horizontal"
        text-color="black"
        active-text-color="skyblue"
        background-color="#fff"
        @select="handleSelect"
      >
        <el-menu-item index="1">首页</el-menu-item>
        <el-submenu index="2">
          <template slot="title">一砖一瓦</template>
          <el-menu-item index="2-1">选项1</el-menu-item>
          <el-menu-item index="2-2">选项2</el-menu-item>
          <el-menu-item index="2-3">选项3</el-menu-item>
        </el-submenu>

        <el-submenu index="3">
          <template slot="title">公司业务</template>
          <el-menu-item index="3-1">选项1</el-menu-item>
          <el-menu-item index="3-2">选项2</el-menu-item>
          <el-menu-item index="3-3">选项3</el-menu-item>
        </el-submenu>

        <el-submenu index="4">
          <template slot="title">专题活动</template>
          <el-menu-item index="4-1">选项1</el-menu-item>
          <el-menu-item index="4-2">选项2</el-menu-item>
          <el-menu-item index="4-3">选项3</el-menu-item>
        </el-submenu>

        <el-submenu index="5">
          <template slot="title">新闻资讯</template>
          <el-menu-item index="5-1">选项1</el-menu-item>
          <el-menu-item index="5-2">选项2</el-menu-item>
          <el-menu-item index="5-3">选项3</el-menu-item>
        </el-submenu>

        <el-menu-item index="6">分支机构</el-menu-item>
        <el-menu-item index="7">联系我们</el-menu-item>
      </el-menu>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1",
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style scoped>
.header {
  display: flex;
  position: fixed;
  /* position: relative; */
  width: 100%;
  height: 60px;
  z-index: 11;
  background: white;
  border-top: 1px solid #EEEEEE;
  border-bottom: 1px solid #EEEEEE;
}
.left-logo {
  margin-left: 10px;
}
.right-nav {
  position: absolute;
  right: 0;
}

</style>