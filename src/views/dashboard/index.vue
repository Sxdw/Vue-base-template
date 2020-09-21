<template>
<div>

    <div class="some">
        <div class="element element-one">
            <i class="el-icon-s-custom wh"></i>
            <div class="ok">
                <h3>今日访问</h3>
                <div class="uh">18345</div>
            </div>
        </div>
        <div class="element element-two">
            <i class="el-icon-s-data wh"></i>
            <div class="ok">
                <h3>总计人数</h3>
                <div class="uh">18985</div>
            </div>
        </div>
        <div class="element element-onc">
            <i class="el-icon-s-marketing wh"></i>
            <div class="ok">
                <h3>历史记录</h3>
                <div class="uh">83726</div>
            </div>
        </div>
    </div>
    <div class="element-oil">
        <h3>用户信息</h3>
        <el-table :data="tableData" border style="width: 100%">
            <el-table-column prop="a" label="日期" width="180"></el-table-column>
            <el-table-column prop="b" label="姓名" width="180"></el-table-column>
            <el-table-column prop="c" label="地址"></el-table-column>
            <el-table-column prop="d" label="标签" width="100" :filters="[{ text: '家', value: '家' }, { text: '公司', value: '公司' }]" :filter-method="filterTag" filter-placement="bottom-end">
                <template slot-scope="scope">
                    <el-tag :type="scope.row.tag === '家' ? 'primary' : 'success'" disable-transitions>家</el-tag>
                </template>
            </el-table-column>
        </el-table>
    </div>
    <div>
        <el-calendar class="liop" v-model="value"></el-calendar>
    </div>
</div>
</template>

<script>
import {
    mapGetters
} from "vuex";

export default {
    data() {
        return {
            tableData: [{
                a: "2016-05-02",
                b: "王小虎",
                c: "上海市普陀区金沙江路 1518 弄",
                d: "家",
            }, ],
            value: new Date(),
        };
    },
    methods: {
        formatter(row, column) {
            return row.address;
        },
        filterTag(value, row) {
            console.log(row);
            return row.tag === value;
        },
        filterHandler(value, row, column) {
            const property = column["property"];
            return row[property] === value;
        },
    },
    created() {},
};
</script>

<style>
html,
body {
    background-color: #f0f2f5;
    position: relative;
}

.some {
    padding: 10px;
    margin: 20px;

    display: flex;
}

.element {
    display: flex;
    border-radius: 4px;
    justify-content: center;
    align-items: center;
    border: 1px solid rgb(243, 230, 230);
    flex: 1;
    height: 150px;
}

.element-one {
    margin-left: 2px;
    font-size: 19px;
    background: #fff;
}

.element-two {
    font-size: 19px;
    margin: 0px 20px;
    background: #fff;
}

.element-onc {
    font-size: 19px;
    background: #fff;
}

.wh {
    font-size: 60px;
    color: rgb(158, 158, 158);
    margin-right: 56px;
    color: #34bfa3;
}

.element-oil {
    padding: 20px;
    margin: 10px;
}

.uh {
    margin-top: 10px;
    color: rgb(158, 158, 158);
}

.ok {
    margin-left: 120px;
}

.liop {
    padding: 1px;
    margin: 30px;
    width: 500px;
    color: #34bfa3;
}
</style>
