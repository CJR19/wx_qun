<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Layout/Header.vue';

const HeaderRoutes = [
  { path: '/', name: 'Home' },
  { path: '/about', name: '会话' },
  { path: '/Home', name: '历史消息' },
  { path: '/Login', name: '群发助手'},
  { path: '/Login', name: '朋友圈'},
  { path: '/Login', name: '客户中心'},
  { path: '/Login', name: '报表统计'},
  { path: '/Login', name: '设计'}
]

</script>

<template>
  <Header :routes="HeaderRoutes" />
  <RouterView />
</template>

<style>
</style>
