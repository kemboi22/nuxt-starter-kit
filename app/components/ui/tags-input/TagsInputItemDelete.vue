<script setup lang="ts">
import type { TagsInputItemDeleteProps } from 'reka-ui'

import type { HTMLAttributes } from 'vue'
import { Cancel01Icon } from '@hugeicons/vue'
import { reactiveOmit } from '@vueuse/core'
import { cn } from 'cn'
import { TagsInputItemDelete, useForwardProps } from 'reka-ui'

const props = defineProps<TagsInputItemDeleteProps & { class?: HTMLAttributes['class'] }>()

const delegatedProps = reactiveOmit(props, 'class')

const forwardedProps = useForwardProps(delegatedProps)
</script>

<template>
  <TagsInputItemDelete v-bind="forwardedProps" :class="cn('flex rounded bg-transparent mr-1', props.class)">
    <slot>
      <Cancel01Icon class="w-4 h-4" />
    </slot>
  </TagsInputItemDelete>
</template>
