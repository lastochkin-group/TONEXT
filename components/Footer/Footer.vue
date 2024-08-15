<script setup>

    import { Icon } from '@iconify/vue'
    import Logo from '../UI/Logos/Logo.vue'
    import LanguageButton from '../UI/Buttons/LanguageButton.vue'
    import NavLink from '../UI/Buttons/NavLink.vue'

    const links = [
        { id: 0, href: '#', title: 'Главная' },
        { id: 1, href: '#', title: 'Faq' },
        { id: 2, href: '#', title: 'Как начать?' },
        { id: 3, href: '#', title: 'Smart-contract' },
        { id: 4, href: '#', title: 'Калькулятор' }
    ]

</script>

<template>
    <header>

        <div class="flex max-lg:flex-col justify-between items-center max-lg:items-start gap-y-4 p-4 container">
            <div class="flex max-lg:justify-between w-full items-center gap-x-6">
                <Logo
                    :isDark="true"
                />

                <LanguageButton
                    title="En"
                    :isDark="false"
                />
            </div>

            <div class="flex w-full">
                <menu class="flex w-full max-lg:flex-col items-center max-lg:items-start gap-6">
                    <ul class="flex max-lg:flex-col max-lg:items-start gap-x-4 gap-y-2 items-center">
                        <li v-for="el, index in links" :key="index">
                            <NavLink 
                                :title="el.title"
                                :link="el.link"
                                :isDark="true"
                            />
                        </li>
                    </ul>

                    <div class="flex gap-x-4 items-center max-lg:w-full lg:hidden">
                        <span class="flex w-fit max-lg:w-full items-center text-[14px] bg-[#EAEDFB] justify-center px-4 h-[45px] gap-x-2 rounded-full text-[#12172D]">
                            <span>1 TON - $4.89</span>
                        </span>
                    </div>
                </menu>
            </div>
        </div>

    </header>
</template>