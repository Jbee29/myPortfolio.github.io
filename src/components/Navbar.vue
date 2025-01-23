<script setup>
import { ref } from 'vue';

const Menu = ref ([
    {name: 'About', href: '#about'},
    {name: 'Experience', href: '#experience'},
    {name: 'Projects', href: '#projects'},
]);

const contact = ref ([
    {name: 'Contact', href: '#contact'},
])

const isMenuOpen = ref(false);
const scrollToSection = (href) => {
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if (section){
        section.scrollIntoView({ behavior: 'smooth' });
    }
};
</script>

<template>
    <section>
        <header class="flex justify-between items-center p-6 bg-opacity-50 relative z-20">
            <div class="text-white text-3xl font-bold pl-6">
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                    JBEE
                </span>
            </div>
            <!-- Mobile Toggle -->
            <div class="md:hidden z-30">
                <button type="button" class="block focus:outline-none" @click="isMenuOpen = !isMenuOpen">
                    <span v-if="isMenuOpen" class="text-5xl">
                        <img src="http://img.icons8.com/ios-filled/100/ffffff/delete-sign.png" alt="close" width="50"
                            height="50">
                    </span>
                    <span v-else class="text-5xl">
                        <img src="http://img.icons8.com/ios-filled/100/ffffff/menu--v6.png" alt="close" width="50"
                            height="50">
                    </span>
                </button>
            </div>
            <!-- Navbar Link -->
            <nav
            :class="['fixed inset-0 z-20 flex flex-col items-center justify-center bg-black md:relative md:bg-transparent md:flex md:justify-between md:flex-row',
            isMenuOpen ? 'block' : 'hidden']">
                <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                    <li v-for="item in Menu" :key="item.name">
                        <a :href="item.href"
                            class="block text-white transition p-3 hover:text-green-300 ease-linear text-2xl ml:text-lg"
                            @click="scrollToSection(item.href)">
                            {{ item.name }}
                        </a>
                    </li>
                    <button v-for="item in contact" :key="item.name"
                    class="rounded-full bg-green-600 hover:bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                        <a :href="item.href"
                            class="block text-black transition p-3 ease-linear text-2xl ml:text-lg"
                            @click="scrollToSection(item.href)">
                            {{ item.name }}
                        </a>                        
                    </button>
                </ul>
            </nav>
        </header>
    </section>
</template>