<template>
<div>
<div class="command-panel">
    <div>
        <el-button style="margin-right:50px;" type="primary" size="small" @click="exportExcel()" icon="el-icon-download">导出</el-button>
        <el-button type="primary" size="small" icon="el-icon-plus">补录</el-button>
        <el-button type="primary" size="small" icon="el-icon-edit">修改</el-button>
        <el-button type="primary" size="small" icon="el-icon-delete">删除</el-button>
    </div>
    <div>汇总: 99999 KG</div>
</div>

<el-dialog title="formTitle" :visible.sync ="showDlg" :close-on-click-modal="false" width="700px" 
    :show-close="true">    
    <el-form class="reportEditForm" ref="addForm" :model="addForm" label-width="100px">
        <el-form-item label='物料类型：' >
            <el-input size="small" clearable disabled value="啊手动阀"></el-input>
        </el-form-item>
        <el-form-item label='物料：' >
            <el-input size="small" clearable disabled value="噶是"></el-input>
        </el-form-item>

        <el-form-item label='qqq：' >
            <el-select  size="small" clearable v-model="addForm.warehouseId">
            </el-select>
        </el-form-item>
        <el-form-item label='sss：' >
            <el-input clearable size="small" 
                v-model.trim="addForm.positionName">
            <i slot="suffix" class="el-input__icon el-icon-search"></i>
            </el-input>
        </el-form-item>        

        <el-form-item label='啊啊是：' >
            <el-date-picker size="small" v-model="addForm.beginDate" type="date" format="yyyy-MM-dd"></el-date-picker>
        </el-form-item>
        <el-form-item label='报表：' >
            <el-input v-model="addForm.stockInUserName" size="small" maxlength="20"
                suffix-icon="el-icon-search"  clearable></el-input>                
        </el-form-item>

        <el-form-item label='aaa：'>
            <el-select  size="small" clearable v-model="addForm.furnaceId">
            </el-select>
        </el-form-item>
        <el-form-item label='bbb：'>
            <el-input size="small" clearable v-model="addForm.productBatch"/>
        </el-form-item>

        <el-form-item label="ccc：">
            <el-select size="small" clearable v-model="addForm.drossingType">
            </el-select>
        </el-form-item>
        <el-form-item label="ddd：">
            <el-select size="small" clearable v-model="addForm.equipmentId">
            </el-select>
        </el-form-item>
    </el-form>
    <div slot="footer" class="dialog-footer">
        <el-button size="small" @click.native="showDlg = false">取消</el-button>
        <el-button size="small" type="primary" @click.native="showDlg = false">确定</el-button>
    </div>
</el-dialog>

</div>
</template>

<script>

export default {
    data() {
        return {
            addForm: {},
            showDlg: false,

        }
    },   
    props: {
        changeDataFlg: false,
    },
    watch: {
        changeDataFlg: {
            handler(n) {
                if (!n) return;
                this.showDlg = true;
                this.$emit('update:changeDataFlg', false);
            }
        }
    },    
    
}
</script>

<style lang="scss" scoped>

.reportEditForm {
    display: flex;
    flex-wrap: wrap;   //默认是不折行
    .el-form-item {
        width: 315px; 
    }
}
  .command-panel {
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
  }
</style>