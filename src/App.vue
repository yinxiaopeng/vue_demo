<template>
  <!-- 模板部分：HTML 结构，使用 Vue 指令绑定数据/事件 -->
  <div id="app">
    <h1>{{ message }}</h1>
    <button @click="changeMessage">点击修改文字</button>
    <!-- 引入自定义组件 -->
    <MyFirstComponent />
  </div>
</template>

<script setup>
// 脚本部分：Vue 3 组合式 API（setup 语法糖），处理逻辑/数据
// 1. 定义响应式数据
import { ref } from 'vue'
const message = ref('你好，Vue！')

// 2. 定义事件处理函数
const changeMessage = () => {
  message.value = 'Vue 真简单！'
}

// 3. 引入自定义组件
import MyFirstComponent from './components/MyFirstComponent.vue'
</script>

<style scoped>
/* 样式部分：scoped 表示样式仅作用于当前组件 */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button {
  padding: 8px 16px;
  background: #42b983;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
