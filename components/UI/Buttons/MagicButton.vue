<script setup>
    import { computed } from 'vue'
    import { Icon } from '@iconify/vue'

    const props = defineProps({
        icon: {
            type: String,
            required: false
        },
        title: {
            type: String,
            required: true,
        },
        link: {
            type: String,
            required: true,
        },
        state: {
            type: String,
            default: 'basic', // Возможные значения: 'basic', 'hover', 'active', 'disabled'
        },
        disabled: {
            type: Boolean,
            default: false,
        },
    })

    const buttonClass = computed(() => {
        switch (props.state) {
            case 'active':
                return 'text-white border-[#FFFFFF20] bg-button_dark_color'
            case 'disabled':
                return 'text-white border-[#FFFFFF20] bg-button_dark_color opacity-25 cursor-not-allowed'
            default: // 'basic'
                return 'text-white border-transparent hover:text-blue'
        }
    })

const gradientClass = computed(() => {
  if (props.disabled) {
    return 'bg-bg-transparent'
  }
  return 'bg-gradient-radial from-[#0098EA] to-transparent'
})
</script>

<template>
  <nuxt-link 
    :to="link"
    :class="[
      'relative overflow-hidden text-[14px] flex w-full items-center justify-start px-4 py-2.5 rounded-lg border transition-all',
      buttonClass,
    ]"
    :aria-disabled="disabled"
  >
    <div v-if="state !== 'basic'" :class="['absolute inset-0 rounded-lg', gradientClass]" />

    <div class="relative flex items-center gap-2 z-10">
      <Icon :icon="icon" :class="['text-[24px]', (state === 'active' || state === 'disabled') && 'text-blue']" />
      <span>{{ title }}</span>
    </div>

    <div v-if="state !== 'basic'">
        <div class="absolute right-2 top-2 w-1.5 h-1.5 bg-blue rounded-full"></div>
        <div class="absolute right-1 top-5 w-[2px] h-[2px] bg-blue rounded-full"></div>
        <div class="absolute right-3 top-7 w-[2px] h-[2px] bg-blue rounded-full"></div>
        <div class="absolute right-6 top-5 w-1 h-1 bg-blue rounded-full"></div>
        <div class="absolute right-6 top-8 w-1 h-1 bg-blue rounded-full"></div>
        <div class="absolute right-4 top-9 w-[2px] h-[2px] bg-blue rounded-full"></div>
    </div>

  </nuxt-link>
</template>

<style scoped>
    .bg-gradient-radial {
        background-image: radial-gradient(circle at 50% 150%, #0098EA, transparent 50%);
        filter: blur(20px);
        transform: scale(1.2);
    }
</style>
