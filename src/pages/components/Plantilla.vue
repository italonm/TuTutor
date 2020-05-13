<template>
<el-container style="height:100%;position:relative">
  <div class="top-bg"></div>
  <el-header class="head" style="height:20%;">
    <el-row style="width:100%" type="flex" class="row-bg" justify="space-around">
      <el-col :span="6"><div class="bg-purple">
        <h2><i class="fas fa-users"></i>&nbsp;Usuarios</h2>
      </div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple-light">
        <el-input placeholder="Buscar usuario" v-model="input">
        <i slot="prefix" class="el-input__icon el-icon-search"></i>
        </el-input>
      </div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple">
      <el-button type="primary" icon="fas fa-user-plus">&nbsp;Agregar</el-button>
      </div></el-col>
  </el-row>
  </el-header>
  <el-main style="height:80%">
    <el-table :data="tableData"   style="width: 100%;border-radius: 25px 25px 25px 25px" height="100%" :row-class-name="tableRowClassName">
    <el-table-column
      prop="date"
      label="Fecha"
      width="180">
      
    </el-table-column>
    <el-table-column
      prop="name"
      label="Nombre"
      width="180">
    </el-table-column>
    <el-table-column
      prop="address"
      label="Dirección">
    </el-table-column>
  </el-table>
  </el-main>
  
  
</el-container>
</template>

<script>
  export default {
    data() {
      return {
        input: '',
        tableData: [
        {
          date: '2016-05-03',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-02',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-04',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }, {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles'
        }]
      }
    },
    methods: {
      tableRowClassName({ rowIndex}) {
        if (rowIndex === 1) {
          return 'warning-row';
        } else if (rowIndex === 3) {
          return 'success-row';
        }
        return '';
      }
    },
  }
</script>
<style lang="scss" scoped>
.el-input__inner {
  border-radius: 25px !important;
}
.top-bg {
        height: 200px;
        position: absolute;
        z-index: 0;
        top: 0;
        right: 0;
        left: 0;
        background-color: rgb(170, 207, 221);
        display: block;
        pointer-events:none;
    }
.head {
  color: rgb(0, 0, 0) !important;
  text-align: center;
  line-height: 60px;
}
  .el-table .warning-row {
    background: oldlace;
  }

  .el-table .success-row {
    background: #a8d192;
  }
  .el-row {
    margin-bottom: 20px;
  }
  .el-row:last-child{
    margin-bottom: 0;
  }
  .el-col {
    border-radius: 4px;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
    top:50% !important;
                transform: translateY(-50%)!important;
                position: relative !important;
  }
  .row-bg {
    padding: 10px 0;
  }
  .demo-input-label {
    display: inline-block;
    width: 130px;
  }
</style>