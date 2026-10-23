<script setup lang="ts">
import type { HTMLAttributes } from 'vue'

import { Loading03Icon } from '@hugeicons/vue'
import { cn } from 'cn'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()
</script>

<template>
  <Loading03Icon role="status" aria-label="Loading" :class="cn('size-4 animate-spin', props.class)" />
</template>
