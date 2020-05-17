<template>
  <div>
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>部署</span>
      </div>
      <div class="deploy-radio">
        <el-radio v-model="radio1" label="1" border>dev</el-radio>
        <el-radio v-model="radio1" label="2" border>fat</el-radio>
      </div>
      <el-row :gutter="12">
        <el-col :span="8" class="deploy-col">
          <el-card shadow="always">
            <div class="card-div">
              <span>1天前</span>
            </div>
            <div>
              <span class="card-env">fat:integration</span>
              <span class="card-user">honey.rao</span>
            </div>
            <el-divider />
            <div class="card-opt">
              <span class="card-id">ID:52636</span>
              <el-button type="text" class="card-btn">部署</el-button>
            </div>
          </el-card>
        </el-col>
        <el-col :span="8" class="deploy-col">
          <el-card shadow="always">
            <div class="card-div">
              <span>1天前</span>
            </div>
            <div>
              <span class="card-env">fat:integration</span>
              <span class="card-user">honey.rao</span>
            </div>
            <el-divider />
            <div class="card-opt">
              <span class="card-id">ID:52636</span>
              <el-button type="text" class="card-btn">部署</el-button>
            </div>
          </el-card>
        </el-col>
        <el-col :span="8" class="deploy-col">
          <el-card shadow="always">
            <div class="card-div">
              <span>1天前</span>
            </div>
            <div>
              <span class="card-env">fat:integration</span>
              <span class="card-user">honey.rao</span>
            </div>
            <el-divider />
            <div class="card-opt">
              <span class="card-id">ID:52636</span>
              <el-button type="text" class="card-btn">部署</el-button>
            </div>
          </el-card>
        </el-col>
        <el-col :span="8" class="deploy-col">
          <el-card shadow="always">
            <div class="card-div">
              <span>1天前</span>
            </div>
            <div>
              <span class="card-env">fat:integration</span>
              <span class="card-user">honey.rao</span>
            </div>
            <el-divider />
            <div class="card-opt">
              <span class="card-id">ID:52636</span>
              <el-button type="text" class="card-btn">部署</el-button>
            </div>
          </el-card>
        </el-col>
      </el-row>
      <div>
        <el-table :data="tableData" border style="width: 100%">
          <el-table-column prop="pod" label="Pod名称" width="180" />
          <el-table-column prop="master_ip" label="宿主机IP" width="180" />
          <el-table-column prop="contanier_ip" label="容器IP" />
          <el-table-column prop="log" label="日志" />
          <el-table-column prop="state" label="容器状态" />
          <el-table-column prop="start_time" label="启动时间" />
          <el-table-column prop="manage" label="管理">
            <template slot-scope="scope">
              <el-button type="text" size="small" @click="handleClick(scope.row)">查看</el-button>
              <el-button type="text" size="small">编辑</el-button>
            </template>
          </el-table-column>
        </el-table>
      </div>
    </el-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      radio1: '1',
      tableData: [{
        pod: '2016-05-02',
        master_ip: '192.168.199.1',
        contanier_ip: '上海市普陀区金沙江路 1518 弄',
        log: 'aaa',
        state: 'success',
        start_time: '2020-01-01'
      },
      {
        pod: '2016-05-02',
        master_ip: '192.168.199.1',
        contanier_ip: '上海市普陀区金沙江路 1518 弄',
        log: 'aaa',
        state: 'success',
        start_time: '2020-01-01'
      }]
    }
  }
}
</script>

<style scoped>
.deploy-radio {
    width: 300px;
    margin: 20px auto;
}

.deploy-col {
    margin-bottom: 10px;
}

.card-div {
    text-align: center;
}

.card-env {
    margin-left:0px;
}

.card-user {
    float:right;
}

.card-opt {
    text-align: right;
}

.card-id {
    float: left;
    margin-top: 12px;
}
</style>
