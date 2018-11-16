<template>
    <div id="Carousel">
        <div class="block">
            <el-carousel :autoplay="false" height="300px">
                <template v-for="(img,index) in imgs">
                    <el-carousel-item :style="{background:'url(./static/images/'+img+(img=='banner3'?'.png':'.webp')+') no-repeat',backgroundSize:'cover'}" :key="index">
                        <h3>{{ img }}</h3>
                        <!-- <img :src="'./static/images/'+img+'.webp'" :alt="img"> -->
                        <!-- <img :src="'./assets/images/'+img+'.webp'" :alt="img"> error-->
                        <!-- <img :src="require('./assets/images/'+img+'.webp')" :alt="img"> error -->
                    </el-carousel-item>
                </template>
            </el-carousel>
            <div class="test">

            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'Carousel',
    data(){
        return {
            imgs:['banner1','banner2','banner3']
        }
    }
}
</script>
<style>
.el-carousel__button{
    height:14px;
    width:40px;
    border-radius:10px;
    background:#0AC373;
}
.el-carousel__item h3 {
    line-height: 300px;
}

.el-carousel__item:nth-child(2n) {
    /* background-color: #99a9bf; */
}

.el-carousel__item:nth-child(2n+1) {
    /* background-color: #d3dce6; */
}
</style>
<style scoped>
.test{
    height:10px;
    /* background:url(./assets/images/logo.png) */
}
</style>