<template>
	<view class="container">
    <!-- 使用子组件，组件名和 import 变量名一致 -->
    <Userinfo 
      avatar="/static/image.png" 
      username="张三" 
    />
    <Userinfo 
      avatar="/static/logo.png" 
      username="李四" 
    />
    <Userinfo 
      avatar="/static/image.png" 
      :username="name" 
    />
    <text>hello world</text>
	</view>
</template>

<script setup>
// 正确路径：和实际文件结构完全一致（注意大小写和文件夹层级）
import Userinfo from '@/components/userinfo/userinfo.vue'
import { ref } from 'vue'
// 定义一个响应式变量，用于存储用户名
const name = ref('王五')
</script>

<style scoped lang="scss">
.container{
  padding: 20rpx;
}
</style>