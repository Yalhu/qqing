<template>
    <div id="teachers">
        <h3>海量师资等你选</h3>
        <p>全国超30000名专业教师、实名认证全方位严格筛选、大数据支持教师科学评级</p>
        <el-row style="margin-bottom:20px;"  v-for="val in Math.ceil(teachers.length/4)" :key="val">
            <!-- <el-col :span="5" v-for="(teacher,index) in teachers.slice(val-1,4)" :key="teacher.id"  :offset="index > 0 ? 1 : 0"> -->
            <el-col :span="6" v-for="(teacher) in teachers.slice(val-1,4)" :key="teacher.id">
                <el-card :body-style="{ padding: '0px' }">
                    <img src="/static/images/hamburger.png" class="image">
                    <div style="padding: 14px;">
                        <span>{{teacher.name}}</span>
                        <p>{{teacher.description}}</p>
                        <div class="bottom clearfix">
                            <el-button type="text" class="button">{{teacher.tag}}</el-button>
                            <time class="time">{{ teacher.teachered }}</time>
                        </div>
                    </div>
                </el-card>
            </el-col>
        </el-row>
        <el-row>
            <el-button type="success">查看更多优秀老师</el-button>
        </el-row>
    </div>
</template>
<script>
export default {
    name:'Teachers',
    data(){
      return {
          teachers:[{
            id:101,
            name:'teach1',
            description:'教龄11年|在线&上门|300条好评',
            tag:'最佳老师',
            teachered:2480
        },{
            id:102,
            name:'teach2',
            description:'教龄21年|在线&上门|1300条好评',
            tag:'最佳老师',
            teachered:4480
        },{
            id:103,
            name:'teach3',
            description:'教龄11年|在线&上门|300条好评',
            tag:'最佳老师',
            teachered:2480
        },{
            id:104,
            name:'teach4',
            description:'教龄11年|在线&上门|300条好评',
            tag:'最佳老师',
            teachered:2480
        },{
            id:105,
            name:'teach5',
            description:'教龄11年|在线&上门|300条好评',
            tag:'最佳老师',
            teachered:2480
        },{
            id:106,
            name:'teach6',
            description:'教龄11年|在线&上门|300条好评',
            tag:'最佳老师',
            teachered:2480
        }]
      }
  }
}
</script>
<style scoped>
.el-col-6{
    padding:0 10px;
}

#teachers{
    width:80%;
    margin:0 auto;
    text-align:center;
}
.time {
    float:right;
    font-size: 13px;
    color: #999;
}

.bottom {
    margin-top: 13px;
    line-height: 12px;
}

.button {
    padding: 0;
    float: left;
}

.image {
    width: 100%;
    display: block;
}

.clearfix:before,
.clearfix:after {
    display: table;
    content: "";
}

.clearfix:after {
    clear: both
}

</style>

