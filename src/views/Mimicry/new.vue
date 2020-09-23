<template>
<div>
    <div class="cuuo">
        <div class="drop-shadow">
            <i class="el-icon-d-caret"></i>
        </div>
        <div class="drop-shadow">
            <i class="el-icon-microphone"></i>
        </div>
        <div class="drop-shadow">
            <i class="el-icon-watch-1"></i>
        </div>
        <div class="drop-shadow">
            <i class="el-icon-truck"></i>
        </div>
        <div class="drop-shadow">
            <i class="el-icon-truck"></i>
        </div>
        <div class="drop-shadow">
            <i class="el-icon-truck"></i>
        </div>
        <div class="drop-shadow">
            <i class="el-icon-truck"></i>
        </div>
        <div class="drop-shadow">
            <i @click="submit" class="el-icon-truck"></i>
        </div>
    </div>
</div>
</template>

<script>
export default {};
</script>

<style>
.cuuo {
    display: flex;

    background: #ecf0f3;
}

.drop-shadow {
    padding: 10px;
    margin: 20px;
    width: 100px;
    height: 100px;
    border-radius: 20px;
    box-shadow: 18px 18px 30px #d1d9e6, -18px -18px 30px #fff;
}

.el-icon-d-caret {
    display: flex;
    justify-content: center;
    font-size: 60px;
    margin-top: 15px;
    color: #c5c5c5;
}

.el-icon-microphone {
    display: flex;
    justify-content: center;
    font-size: 60px;
    margin-top: 15px;
    color: #c5c5c5;
}

.el-icon-watch-1 {
    display: flex;
    justify-content: center;
    font-size: 60px;
    margin-top: 15px;
    color: #c5c5c5;
}

.el-icon-truck {
    display: flex;
    justify-content: center;
    font-size: 60px;
    margin-top: 15px;
    color: #c5c5c5;
}
</style>
