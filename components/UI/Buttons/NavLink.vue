<script setup>
    import { computed } from 'vue'

    const props = defineProps({
    title: {
        type: String,
        required: true,
    },
    link: {
        type: String,
        required: true
    },
    state: {
        type: String,
        default: 'basic', // Возможные значения: 'basic', 'active', 'disabled'
    },
    disabled: {
        type: Boolean,
        default: false,
    },
    isDark: {
        type: Boolean,
        default: false
    }
    })

    const linkClass = computed(() => {
        switch (props.state) {
            case 'active':
                return 'text-blue'
            case 'disabled':
                return props.isDark ? 'text-[#12172D]' : 'text-white', 'cursor-not-allowed opacity-25'
            default:
                return props.isDark ? 'text-[#12172D]' : 'text-white'
        }
    })
</script>

<template>
  <nuxt-link :to="link"
    :class="[
      'text-[14px] w-fit transition-colors duration-300',
      linkClass,
      {
        'hover:underline': state === 'basic' && !disabled
      }
    ]"
    :href="disabled ? null : '#'"
    :aria-disabled="disabled"
  >
    {{ title }}
    </nuxt-link>
</template>
