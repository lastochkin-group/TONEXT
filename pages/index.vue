<script setup>
  import { onBeforeMount, ref } from 'vue';
  import { useI18n } from 'vue-i18n';

  import Header from '../components/Header/Header.vue';
  import HeroSection from '../components/HeroSection/HeroSection.vue';
  import Calculator from '../components/Calculator/Calculator.vue';
  import StepsSection from '~/components/Steps/StepsSection.vue';
  import AdvantagesSection from '~/components/Advantages/AdvantagesSection.vue';
  import FAQSection from '~/components/FAQ/FAQSection.vue';
  import Footer from '~/components/Footer/Footer.vue';

  const { locale, availableLocales, loadLocaleMessage } = useI18n();
  const isReady = ref(false);

  async function loadLocale() {
    const currentLocale = locale.value;

    if (!availableLocales.includes(currentLocale)) {
      await loadLocaleMessage(currentLocale);
    }

    isReady.value = true;
  }

  onBeforeMount(async () => {
    await loadLocale();
  });
</script>

<template>
  <div v-if="isReady">
    <Header />

    <main class="flex flex-col bg-bg_color rounded-t-3xl">
      <HeroSection />
      <Calculator />
      <StepsSection />
      <div class="flex flex-col gap-y-12">
        <AdvantagesSection />
        <FAQSection />
      </div>

      <Footer />
    </main>
  </div>
</template>
