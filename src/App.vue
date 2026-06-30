<script setup lang="ts">
import { ref } from 'vue'
import { KlineChart } from '@363045841yyt/klinechart'
import demoData from './demo-data.json'

const currentTheme = ref<'light' | 'dark'>('dark')
</script>

<template>
  <div class="app-container" :data-theme="currentTheme">
    <KlineChart v-model:theme="currentTheme" :custom-data="demoData" />
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html, body, #app {
  height: 100%;
  width: 100%;
}
.app-container {
  display: flex;
  flex-direction: column;
  height: 100%;
  width: 100%;
}
.app-container[data-theme='dark'] {
  background: #000;
  color: #e5e7eb;
}
</style>
