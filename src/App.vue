<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <!-- 我的git第一次提交，提交项目到远程master -->
    <!-- 我的git第二次提交，提交项目到远程dev -->
    <!-- 我的git第三次次提交，提交项目到远程dev -->
    <!-- 我的git线上修改，在dev仓库-->
    <!-- 我的git第四次提交，提交项目到远程dev，远程dev被修改，解决冲突 -->
    <!-- 我的git第五次提交，提交项目到远程dev，测试add添加一个文件，以及撤销add -->

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
