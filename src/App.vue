<script setup lang="ts"></script>

<template>
  <div class="app-bg">
    <router-view v-slot="{ Component }">
      <transition name="fade" mode="out-in">
        <component :is="Component" />
      </transition>
    </router-view>
  </div>
</template>

<style>
/* 全局默认背景（所有页面） */
.app-bg {
  min-height: 100vh;
  background: linear-gradient(191deg, #d3eeec 4.31%, #ecf3cb 92.6%), #f8f8f8;
}

/* 页面切换动画 */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.4s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
