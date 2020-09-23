<template>
<div>
    <div>
        <el-carousel :interval="4000" type="card" height="300px">
            <el-carousel-item v-for="item in 6" :key="item">
                <h3 class="medium"></h3>
                <img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1600667902510&di=b85fd76118f2e9ab8a78e0abc981b678&imgtype=0&src=http%3A%2F%2Fpic4.zhimg.com%2Fv2-b3c03d5d3de1e23ad964d18cbdb2da00_1200x500.jpg" alt="我怕我没有机会" />
            </el-carousel-item>
        </el-carousel>
    </div>
    <div class="okhg">
        <div class="polhbg">
            <div class="card left"></div>
            <div class="card right"></div>
        </div>
    </div>
</div>
</template>

<script>
export default {};
</script>

<style>
.el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
}

.el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
    background-color: #d3dce6;
}

.okhg {
    /* 定义变量 */
    --bgColor: #f5bbbb;

    /* rgba的四个值分别为：红(R)、绿(G)、蓝(B)、透明度(A) */
    --whiteShadow: -15px -15px 25px rgba(255, 117, 117, 0.5);
    --blackShadow: 15px 15px 25px rgba(110, 40, 40, 0.2);
}

/* 设置一些页面的布局样式 */
.polhbg {
    display: flex;
    margin: 0;
    padding: 0;
    width: 100vh;
    height: 100vh;
    justify-content: center;
    align-items: center;
    background-color: var(--bgColor);
}

.card {
    width: 30vh;
    height: 30vh;
    margin: 45px;
    background-color: var(--bgColor);
    border-radius: 30px;
}

/* 主要部分 */
.left {
    /* 设置外阴影 */
    box-shadow: var(--blackShadow), var(--whiteShadow);
}

.right {
    /* 设置内阴影 */
    box-shadow: inset var(--blackShadow), inset var(--whiteShadow);
}
</style>
