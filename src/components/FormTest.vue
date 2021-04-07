<template>
<div class="formTest">
    <el-form :inline="true" id="filtersFrom" label-width="80px">
        <el-form-item label="部门:">
        <el-select size="small" clearable placeholder="选择部门">
                  <el-option key="a" label="a" value="a"> </el-option>
                  <el-option key="b" label="b" value="b"> </el-option>                  
        </el-select>
        </el-form-item>
        <el-form-item label="用户:">
            <el-input size="small" clearable placeholder="用户" ></el-input>
        </el-form-item>
        <el-form-item label="名称:">
            <el-input size="small" clearable placeholder="名称" ></el-input>
        </el-form-item>
        <el-form-item label="aaa:">
            <el-input></el-input>
        </el-form-item>
    </el-form>    




</div>
</template>

<script>
export default {
    
}
</script>

<style scoped lang="scss">
.formTest {
    display: flex;
    justify-content: space-between;
    height: 45px;
    overflow: hidden;
    &.filtersMore {
        height: auto;
        transition: all 0.5s;
    }
    .filter-btn {
        min-width: 440px;
        line-height: 32px;
    }
    border-bottom: 1px solid #ccc;
    margin-bottom: 20px;
    width: 100%;
    .el-select {
        width: 200px;
    }
    .el-form-item__label,
    .el-form-item__content {
        line-height: 32px;
    }
    .el-input {
        width: 210px;
    }
}

.formTest .el-input {
    // !importanrt可以覆盖父级的样式
    width: 220px;// !important;
}
</style>