<script setup>
    import { ref, onMounted, onUnmounted } from 'vue';

    const isVisible = ref(false);
    const handleScroll = () => {
        isVisible.value = window.scrollY > 300;
    };
    const scrollToTop = () => {
        window.scrollTo({
            top: 0,
            behavior: 'smooth',
        });
    };

    onMounted(() => {
        window.addEventListener('scroll', handleScroll);
    });

    onUnmounted(() => {
        window.removeEventListener('scroll', handleScroll);
    });
</script>

<template>
    <button v-if="isVisible" @click="scrollToTop" class="fixed bottom-4 right-4 bg-green-500 text-black
    rounded-full w-12 h-12 flex items-center justify-center text-xl cursor-pointer transition-opacity duration-300 hover:bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
         ↕
    </button>
</template>