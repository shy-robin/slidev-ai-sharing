<script setup lang="ts">
import ArrowRight from "./ArrowRight.vue";

defineProps({
  index: {
    default: 0,
  },
});
</script>

<template>
  <div class="flex items-center mb-5">
    <div
      class="text-[#666] px-2 rounded-lg"
      :class="{ 'bg-[#5d8392]': index === 0, 'text-white': index === 0 }"
    >
      触发阶段
    </div>
    <ArrowRight />
    <div
      class="text-[#666] px-2 rounded-lg"
      :class="{ 'bg-[#5d8392]': index === 1, 'text-white': index === 1 }"
    >
      输入阶段
    </div>
    <ArrowRight />
    <div
      class="text-[#666] px-2 rounded-lg"
      :class="{ 'bg-[#5d8392]': index === 2, 'text-white': index === 2 }"
    >
      处理阶段
    </div>
    <ArrowRight />
    <div
      class="text-[#666] px-2 rounded-lg"
      :class="{ 'bg-[#5d8392]': index === 3, 'text-white': index === 3 }"
    >
      反馈阶段
    </div>
    <ArrowRight />
    <div
      class="text-[#666] px-2 rounded-lg"
      :class="{ 'bg-[#5d8392]': index === 4, 'text-white': index === 4 }"
    >
      后续阶段
    </div>
  </div>
</template>
