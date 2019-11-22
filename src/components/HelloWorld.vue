<template>
  <div id="main">
    <div class="navigation">
      <el-menu
        :default-active="activeIndex"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
      >
        <el-menu-item index="1">首页</el-menu-item>
        <el-menu-item index="2">最新</el-menu-item>
        <el-menu-item index="3">热门</el-menu-item>
        <el-menu-item index="4">分类</el-menu-item>
      </el-menu>
    </div>

    <div class="carousel">
      <el-carousel :interval="4000" type="card">
        <el-carousel-item v-for="item in 6" :key="item">
          <h3 class="medium">{{ item }}</h3>
        </el-carousel-item>
      </el-carousel>
    </div>

    <!-- <div class="imageList" id="app">
      <el-row
        :gutter="20"
        v-loading="loading"
        :data="tableData"
        style="width: 100%"
      >
        <el-col :span="6" v-for="(item, index) in items" :key="index"
          ><div class="grid-content bg-purple"></div>
          {{ index }}{{ item.message }}</el-col
        >
      </el-row>
    </div> -->
    <div class="imageList" id="app">
      <div :gutter="20" v-loading="loading" :data="tableData" class="dududu">
        <div v-for="(item, index) in items" :key="index" class="du">
          <div class="grid-content bg-purple"></div>
          {{ index }}{{ item.message }}
          
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      activeIndex: "1",
      isCollapse: true,
      loading: false,
      items: [
        { message: "Foo" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" },
        { message: "Bar" }
      ]
    };
  },
  methods: {
    handleOpen(key, keyPath) {},
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}
.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
#main {
  border: 0px solid #cccccc;
}
.carousel {
  margin-top: 20px;
}

.el-row {
  margin-bottom: 40px;
}
.el-col {
  border-radius: 4px;
  margin-top: 20px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  width: 100%;
  height: 100%;
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
}
.row-bg {
  background-color: #f9fafc;
}
.dududu {
  width: 100%;
  position: relative;
  text-align: center;
}
.dududu .du{
  display: inline-block;
  position: relative;
  width: 25vw;
  margin: 2.2vw;
  height: calc(25vw * 0.8 - 0px);
}
</style>
