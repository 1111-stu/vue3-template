<script setup lang="ts">
import { storeToRefs } from 'pinia'
import appStore from '@/store/index'

// Pinia composition API 模式
const { count, doubleCount } = storeToRefs(appStore.useCounter)
const { increment, decrement } = appStore.useCounter
</script>
<template>
  <div>
    <h1 class="title">Pinia composition 模式！</h1>
    <p>
      Pinia state:count=<b>{{ count }}</b>
    </p>
    <p>
      pinia getters:doubleCount=<b>{{ doubleCount }}</b>
    </p>
    <button @click="increment">increment</button>
    <button @click="decrement">decrement</button>
  </div>
</template>

<style lang="scss" scoped>
.title {
  color: $primary-color;
}
</style>
