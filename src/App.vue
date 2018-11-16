<template>
  <div id="app">
    <el-container>
        <el-header class="header" height="80px">
            <Header></Header>
        </el-header>
        <el-main>
            <SubNav></SubNav>
            <Carousel></Carousel>
            <Teachers></Teachers>
        </el-main>
    </el-container>
  </div>
</template>

<script>
import Header from './components/Header'
import SubNav from './components/SubNav'
import Carousel from './components/Carousel'
import Teachers from './components/Teachers'
// import from './components/'

export default {
  name: 'App',
  components: {
    Header,
    SubNav,Carousel,Teachers
  },
}
</script>
<style scoped>
.header{
    padding:0;
}
.el-main{
    padding:0;
}
</style>

