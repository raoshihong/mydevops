<template>
  <div class="deploy">
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>构建</span>
      </div>
      <label>项目名称</label>
      <el-select v-model="value" placeholder="请选择" class="selectitem">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        />
      </el-select>
      <el-button @click="clickShowLog()">日志查看</el-button>
      <!-- 使用ref指定引用组件 -->
      <ShowLog ref="ShowLog" />
      <el-row class="build_branch">
        <el-button>master</el-button>
        <el-button type="primary">intergration</el-button>
        <el-button type="success">intergration2</el-button>
        <el-button type="info">intergration3</el-button>
        <el-button type="warning">production</el-button>
      </el-row>
    </el-card>
    <Deploy />
  </div>
</template>

<script>

import ShowLog from './build/showlog'
import Deploy from './deploy'

export default {
  components: {
    'ShowLog': ShowLog,
    Deploy
  },
  data() {
    return {
      options: [
        {
          value: 'app-cloud-platform',
          label: 'app-cloud-platform'
        },
        {
          value: '选项2',
          label: '双皮奶'
        },
        {
          value: '选项3',
          label: '蚵仔煎'
        },
        {
          value: '选项4',
          label: '龙须面'
        },
        {
          value: '选项5',
          label: '北京烤鸭'
        }
      ],
      value: ''
    }
  },
  methods: {
    clickShowLog() {
      // 通过$refs获取组件对象,并修改组件中暴露的自定义数据属性
      this.$refs.ShowLog.dialogTableVisible = true
    }
  }
}
</script>

<style>
.text {
  font-size: 14px;
}

.item {
  margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}

.box-card {
  margin: 20px 10px;
}

.selectitem {
  margin-left: 10px;
}

.build_branch {
    width: 700px;
    margin: 20px auto;
}

</style>

