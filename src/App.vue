<script setup>
import {ref, shallowRef , computed , watch , nextTick } from 'vue'
import Chart from 'chart.js/auto'
import { B } from 'chart.js/dist/chunks/helpers.core'

const weights=ref([])

const weightChartEl = ref(null)

const weightChart=shallowRef(null)

const weightInput = ref(60.0)

const currentWeight = computed(()=> {
  return weights.value.sort((a,b)=> b.date - a.date)[0] || {weight: 0}
})
</script>

<template>
  <h1>Hello , World! </h1>
</template>
 
<style scoped>

</style>
