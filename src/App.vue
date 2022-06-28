<script setup lang="ts">
import { whenever  } from '@vueuse/core'
import {ref} from 'vue'

const source = ref(false)

whenever(
  source,
  (value) => {
    console.log('当前值',value)
  },
)

const clickedFn = () => {
  source.value = !source.value
}

</script>

<template>
 <div>{{source}}</div>
  <button @click="clickedFn">
    点击按钮
  </button>
</template>