<template>
    <div class="top">
        资讯栏目
    </div>
    <div class="bottom">
        <div class="wrap">
            <el-button type="primary" color="#006AE8">新增</el-button>
            <el-table :data="tableData" header-cell-class-name="headerStyle" border style="width: 100%">
                <el-table-column prop="date" label="栏目名称" />
                <el-table-column prop="name" label="连接地址" />
                <el-table-column prop="address" label="开放客户调整" />
                <el-table-column prop="address" label="是否展示" />
                <el-table-column prop="address" label="操作" />
            </el-table>
        </div>
    </div>
</template>

<script setup lang="ts">

const tableData = [
    {
        date: '2016-05-03',
        name: 'Tom',
        address: 'No. 189, Grove St, Los Angeles',
    },
    {
        date: '2016-05-02',
        name: 'Tom',
        address: 'No. 189, Grove St, Los Angeles',
    },
    {
        date: '2016-05-04',
        name: 'Tom',
        address: 'No. 189, Grove St, Los Angeles',
    },
    {
        date: '2016-05-01',
        name: 'Tom',
        address: 'No. 189, Grove St, Los Angeles',
    },
]


</script>

<style scoped lang="less">
::v-deep .headerStyle {
    background-color: #F4F7FF !important;
    color: black;
}

::v-deep .el-table--border .el-table__cell {
    border-right: none;
}
.top {
    height: 50px;
    line-height: 50px;
    font-size: 16px;
    color: black;
    background-color: #fff;
    padding: 0 20px 20px;
}

.bottom {
    min-height: 208px;
    background: #f5f5f5;
    box-sizing: border-box;
    padding: 0 20px;

    .wrap {
        background-color: #fff;
        width: 100%;
        height: 100%;
        margin-top: 10px;
        padding: 20px;
    }
}

.el-table--fit {
    margin-top: 30px;
}
</style>