<template>
  <div style="margin-left:2%">
    <el-form label-width="130px" size="mini" style="width: 100%;display: inline-block">
      <el-form-item label="调拨单号:" class="right-content-body-tableForm">
       {{info.transferBillCode}}
      </el-form-item>
      <el-form-item label="转出部门:" class="right-content-body-tableForm">
        {{info.outDeptName}}
      </el-form-item>
      <el-form-item label="转出仓库:" class="right-content-body-tableForm">
        {{info.outWarehouseName}}
      </el-form-item>
      <el-form-item label="转入部门:" class="right-content-body-tableForm">
        {{info.inDeptName}}
      </el-form-item>
      <el-form-item label="转入仓库:" class="right-content-body-tableForm">
        {{info.inWarehouseName}}
      </el-form-item>
      <el-form-item label="申请人:" class="right-content-body-tableForm">
        {{info.applierName}}
      </el-form-item>
      <el-form-item label="作废时间:" class="right-content-body-tableForm" v-if="info.cancelDate">
        {{new Date(info.cancelDate).pattern("yyyy-MM-dd")}}
      </el-form-item>
      <el-form-item label="作废操作员:" class="right-content-body-tableForm" v-if="info.cancelDate">
        {{info.cancelPersonName}}
      </el-form-item>
      <el-form-item label="作废原因:" class="right-content-body-tableForm" style="width: 98.2%" v-if="info.cancelDate">
        {{info.cancelReason}}
      </el-form-item>
      <el-form-item label="备注:" class="right-content-body-tableForm" style="width: 98.05%">
        {{info.remarks}}
      </el-form-item>
    </el-form>
  </div>
</template>
<script>
  export default{
    name:"Info",
      props:['info'],
    mounted(){

    },
    data(){
      return{

      }
    },
    methods:{

    }
  }
</script>
<style>

</style>
