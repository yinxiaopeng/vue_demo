<template>
  <div class="custom-component">
    <h3>{{ subTitle }}</h3>
    <p>这是我创建的第一个自定义 Vue 组件！</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
// 子组件的响应式数据
const subTitle = ref('自定义组件标题')
</script>

<style scoped>
.custom-component {
  margin-top: 20px;
  padding: 10px;
  border: 1px solid #eee;
  border-radius: 6px;
}
</style>
