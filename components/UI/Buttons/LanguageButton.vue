<script setup>
  import { computed } from 'vue'
  import { Icon } from '@iconify/vue'
  import { useI18n } from 'vue-i18n'

  const { locale, availableLocales } = useI18n()

  const props = defineProps({
    title: {
      type: String,
      default: false
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

  const buttonClass = computed(() => {
    switch (props.state) {
      case 'active':
        return 'from-[#2A83EB] to-[#1AC9FF] bg-gradient-to-b'
      case 'disabled':
        return props.isDark ? 'bg-button_dark_color text-button_dark_text_color': 'bg-button_color text-button_text_color'
      default:
        return props.isDark ? 'bg-button_dark_color text-button_dark_text_color': 'bg-button_color text-button_text_color'
    }
  })

  function switchLocale(code) {
    locale.value = code
  }

  
</script>


<template>
  <!-- <button v-for="locale in $i18n.locales" :key="locale.code" @click="switchLocale(locale.code)">
    {{ locale.name }}
  </button> -->

  <button
    :class="[
      isDark ? 'border-button_text_color' : 'border-button_dark_text_color',
      'flex w-fit items-center border-[1px] text-[14px] justify-center px-4 h-[45px] gap-x-2 rounded-full transition-colors duration-300',
      buttonClass,
      { 
        'cursor-not-allowed opacity-25': disabled,
        'hover:border-[#FFFFFF40]': state === 'basic' && !disabled
      }
    ]"
    :disabled="disabled"
  >
    <Icon icon="octicon:globe-24" class="text-[20px]" />
    <span>{{ title }}</span>
  </button>

</template>