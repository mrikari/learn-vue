<script setup lang="ts">
const { iconColor, delta } = defineProps<{
  title: string
  iconColor: 'red' | 'blue' | 'orange' | 'pink'
  delta: number
}>()

let iconClass = 'shadow rounded-full text-white w-3 h-3 p-4 flex justify-center items-center'
switch (iconColor) {
  case 'red':
    iconClass += ' bg-red-500'
    break
  case 'orange':
    iconClass += ' bg-orange-500'
    break
  case 'blue':
    iconClass += ' bg-blue-500'
    break
  case 'pink':
    iconClass += ' bg-pink-500'
    break
  default:
    iconClass += ' bg-red-500'
    break
}

let rateClass = 'text-xs font-semibold'
let rateLabel = ''

if (delta > 0) {
  rateLabel = '上昇'
  rateClass += ' text-green-500'
} else if (delta == 0) {
  rateLabel = ''
  rateClass += ' text-gray-500'
} else if (delta > -5) {
  rateLabel = '下降'
  rateClass += ' text-orange-500'
} else {
  rateLabel = '下降'
  rateClass += ' text-red-500'
}
</script>

<template>
  <div class="bg-white rounded shadow-sm">
    <div class="flex flex-col p-3 gap-3">
      <div class="flex flex-row items-center justify-between">
        <div class="flex flex-col">
          <p class="text-gray-400 text-sm font-bold">{{ title }}</p>
          <p class="text-gray-900 text">1,000,000</p>
        </div>
        <div :class="iconClass">A</div>
      </div>
      <div class="flex flex-row gap-3">
        <div class="text-gray-400 text-xs font-semibold">先月から</div>
        <div :class="rateClass">{{ `${delta.toFixed(2)}% ${rateLabel}` }}</div>
      </div>
    </div>
  </div>
</template>
