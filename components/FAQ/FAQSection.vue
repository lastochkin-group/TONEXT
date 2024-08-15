<script setup>

    import { Icon } from '@iconify/vue'
    import DropdownItem from '../UI/Dropdowns/DropdownItem.vue'

</script>

<template>

    <section class="container">
        <div class="bg-[#12172D] rounded-2xl px-4 py-12">
            <div class="flex flex-col gap-y-8">
                <div class="flex z-1 w-1/3 max-lg:w-full max-lg:items-center flex-col gap-y-4">
                    <span class="flex justify-center items-center bg-blue rounded-full w-[45px] aspect-square">
                        <Icon icon="iconamoon:search-light" class="text-[24px] text-white" />
                    </span>

                    <h4 class="font-extrabold text-white text-2xl max-lg:text-center">Часто задаваемые вопросы</h4>
                </div>

                <div class="flex max-lg:flex-col justify-between gap-x-6 gap-y-2">
                    <div class="flex flex-col gap-y-2 w-full">
                        <DropdownItem 
                            title="Какая минимальная сумма вывода?"
                            content="#"
                        />

                        <DropdownItem 
                            title="Как стейкать TON с помощью Tonstakers?"
                            content="Нажмите кнопку «Connect  wallet» в центре или в правом верхнем углу. Затем выберите свой кошелек и подтвердите доступ к приложению Tonstakers."
                        />
                    </div>

                    <div class="flex flex-col gap-y-2 w-full">
                        <DropdownItem 
                            title="Как работает реферальная программа?"
                            content="#"
                        />

                        <DropdownItem 
                            title="Могу ли я выводить без вложений?"
                            content="#"
                        />
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>