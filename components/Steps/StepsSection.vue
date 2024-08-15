<script setup>

    import StepItem from './StepItem.vue'

    const steps = [
        { id: 0, step: '01', title: 'Подключите кошелек', description: 'Подключите кошелек одни из удобных для вас способов. Мы рекомендуем использовать кошелек “Tonkeeper”' },
        { id: 1, step: '02', title: 'Введите сумму и срок', description: 'В поле ввода введите, сумму, которую хотите инвестировать. Так же выбирите период, на который вы хотите инвестировать.' },
        { id: 2, step: '03', title: 'Получайте дивиденды', description: 'Получайте и выводите дивиденды, которые вы заработали.' }
    ]

</script>

<template>
    <section class="container">
       <div class="py-20 px-8 flex flex-col gap-y-6">
            <h2 class="font-extrabold text-[#12172D] text-2xl max-lg:text-center">Начните стейкинг ТОН всего в 3 шага</h2>
            <div class="flex max-lg:flex-col gap-2 justify-between">
                <StepItem 
                    v-for="el, index in steps"
                    :key="index"
                    :step="el.step"
                    :title="el.title"
                    :description="el.description"
                />
            </div>
       </div>
    </section>
</template>