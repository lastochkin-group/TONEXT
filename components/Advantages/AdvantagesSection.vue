<script setup>

    import { Icon } from '@iconify/vue'

</script>

<template>

    <section class="container">
        <div class="bg-[#F7F9FB] rounded-2xl px-4 py-12">
            <div class="flex flex-col gap-y-8">
                <div class="flex z-1 w-1/3 max-lg:w-full max-lg:items-center flex-col gap-y-4">
                    <span class="flex justify-center items-center bg-blue rounded-full w-[45px] aspect-square">
                        <Icon icon="mingcute:rocket-line" class="text-[24px] text-white" />
                    </span>

                    <h4 class="font-extrabold text-[#12172D] text-2xl max-lg:text-center">Преимущества<br />staking TON</h4>
                </div>

                <div class="flex max-lg:flex-col gap-2 justify-between">

                    <div class="from-[#2A83EB] to-[#1AC9FF] bg-gradient-to-b flex flex-col gap-y-6 justify-between rounded-2xl p-4 pb-0 w-full">
                        <div class="flex flex-col gap-y-2">
                            <h5 class="font-extrabold text-xl text-white">Высокий процент дохода</h5>
                            <p class="text-white">Подключите кошелек одни из удобных для вас способов. Мы рекомендуем использовать кошелек “Tonkeeper”</p>
                        </div>

                        <div class="flex justify-center items-center w-full">
                            <img src="../../assets/images/adv_1.png" alt="Mobile App" />
                        </div>
                    </div>

                    <div class="bg-white flex flex-col gap-y-6 justify-between rounded-2xl p-4 pt-0 w-full">
                        <div class="flex justify-center items-center w-full">
                            <img src="../../assets/images/adv_2.png" alt="Mobile App" />
                        </div>

                        <div class="flex flex-col gap-y-2">
                            <h5 class="font-extrabold text-xl text-[#12172D]"><span class="text-blue">Доступность</span> каждому</h5>
                            <p class="text-[#12172D]">Вы можете начать свой путь к ставкам всего с 1 тонны, минуя традиционное требование о минимальной ставке в 10 000 тонн.</p>
                        </div>
                    </div>

                    <div class="bg-[#12172D] flex flex-col gap-y-6 justify-between rounded-2xl p-4 pb-0 w-full">
                        <div class="flex flex-col gap-y-2">
                            <h5 class="font-extrabold text-xl text-white">Децентрализация</h5>
                            <p class="text-white">Ваши активы находятся в безопасности и под вашим контролем благодаря проверенному смарт-контракту на блокчейне TON.</p>
                        </div>

                        <div class="flex justify-center items-center w-full">
                            <img src="../../assets/images/adv_3.png" alt="Mobile App" />
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </section>

</template>