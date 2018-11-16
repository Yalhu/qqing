<template>
    <div id="subNav" >
        <el-menu  class="el-menu-demo" mode="horizontal">
            <template v-for="(grade,key) of grades">
                <el-submenu :index="key" :key="key">
                    <template slot="title">{{key}}</template>
                    <template v-for="(value,clsNum) in grade">
                        <el-menu-item :index="key+clsNum+1" :key="clsNum">{{value+':'+clsNum}}</el-menu-item>
                    </template>
                </el-submenu>
            </template>
        </el-menu>
        <div class="line"></div>
    </div>
</template>
<script>
export default {
    name:'SubNav',
    data(){
        return {
            grades:{
                grade1:['class01','class02','class03','class04','class05','class06'],
                grade2:['class01','class02','class03','class04','class05','class06'],
                grade3:['class01','class02','class03','class04','class05','class06'],
                grade4:['class01','class02','class03','class04','class05','class06'],
                grade5:['class01','class02','class03','class04','class05','class06'],
                grade6:['class01','class02','class03','class04','class05','class06'],
                grade7:['class01','class02','class03','class04','class05','class06'],
                grade8:['class01','class02','class03','class04','class05','class06'],
            }
        }
    }
}
</script>
<style scoped>
#subNav{
    width:80%;
    margin:0 auto;
}
.el-submenu{
    width:12%;
}
</style>

