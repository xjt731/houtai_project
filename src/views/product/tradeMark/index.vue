<template>
    <div>
      <el-button type="primary" icon="el-icon-plus" style="margin:10px 0px">添加</el-button>
      <!-- 表格区域:显示品牌信息
            data:即为表格展示数据---一定是数组
            table:border,设置边框、header-cell-style设置表头的样式外观
            column:label表头文字设置
            label标题设置
            align：标题对其方式
            
            width:设置每一列的宽度（width默认数值代表均分）
       -->
      <el-table style="width: 100%; margin: 10px 0px" border :header-cell-style="{color:'red'}">
        <el-table-column prop="prop" label="序号" width="80px" align="center">
        </el-table-column>
        <el-table-column prop="prop" label="品牌名称" width="width">
        </el-table-column>
        <el-table-column prop="prop" label="品牌LOGO" width="width">
        </el-table-column>
        <el-table-column prop="prop" label="操作" width="width">
        </el-table-column>
      </el-table>
  
      <!-- 分页器
         @size-change="handleSizeChange"
         @current-change="handleCurrentChange"
  
         pagination:
         current-page代表当前第几页、
         page-size一页显示几条数据、
         page-sizes可以设置每一页展示几条数据
         total:一共展示多少条数据
         layout:可以概念分页器布局设置
  
       -->
      <el-pagination
        style="text-align:center"
        :current-page="1"
        :page-sizes="[3,5,10]"
        :page-size="3"
        :pager-count='9'
        background
        prev-text="上一页"
        next-text="下一页"
        layout="prev, pager, next, jumper,->,total,sizes"
        :total="99">
      </el-pagination>
    </div>
  </template>
  
  <script>
  export default {
    name: "tradeMark",
  };
  </script>
  
  <style scoped>
  </style>
  