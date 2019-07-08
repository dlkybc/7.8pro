<template>
<div>
  <el-carousel :interval="5000" arrow="always">
    <el-carousel-item v-for="item in sliders" :key="item.id">
      <img :src="item.img" alt="">
    </el-carousel-item>
  </el-carousel>
  <h4>表格</h4>
   <el-table
    :data="tableData"
    stripe
    style="width: 100%">
    <el-table-column
      prop="date"
      label="日期"
      width="180">
    </el-table-column>
    <el-table-column
      prop="name"
      label="姓名"
      width="180">
    </el-table-column>
    <el-table-column
      prop="address"
      label="地址">
    </el-table-column>
  </el-table>
</div>



</template>

<script>
export default {

  data(){
    return {
     sliders:[{
  "id": 1,
  "name": "榴莲",
  "price": 300,
  "info": "大户肯定汇顶科技",
  "img": "https://img.alicdn.com/bao/uploaded/TB2XOJldQKWBuNjy1zjXXcOypXa_!!3034261223-0-beehive-scenes.jpg_180x180xzq90.jpg_.webp"
}, {
  "id": 2,
  "name": "葡萄",
  "price": "200",
  "info": "正宗红富士1",
  "img": "https://img.alicdn.com/bao/uploaded/TB23JankiOYBuNjSsD4XXbSkFXa_!!2233100926-0-beehive-scenes.jpg_180x180xzq90.jpg_.webp"
}, {
  "id": 3,
  "name": "榴莲",
  "price": 3,
  "info": "正宗红富士",
  "img": "https://img.alicdn.com/bao/uploaded/TB2hFc9bYBmpuFjSZFuXXaG_XXa_!!2775733463.jpg_180x180xzq90.jpg_.webp"
}, {
  "id": 4,
  "name": "桃子",
  "price": 20,
  "info": "正宗红富士",
  "img": "https://img.alicdn.com/bao/uploaded/TB2HloolXXXXXXzXpXXXXXXXXXX_!!1759185958.jpg_180x180xzq90.jpg_.webp"
},],
tableData: [{
          date: '2016-05-02',
          name: '闫百仓',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 5588 弄'
        }, {
          date: '2016-05-01',
          name: '张三',
          address: '上海市普陀区金沙江路 9987 弄'
        }, {
          date: '2016-05-03',
          name: '李四',
          address: '上海市普陀区金沙江路 6325 弄'
        }]
    }
  }

}
</script>
<style>
  .el-carousel__item img {
    width:100%;
    height: 100%;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
  tr{
    width:100%;
  }
</style>
