<script setup>
    import { DotLottieVue } from '@lottiefiles/dotlottie-vue';
    import resume from '../assets/BERNARD.pdf';
    import AOS from 'aos';
    import 'aos/dist/aos.css';

    AOS.init();
</script>

<template>
    <Section class="relative w-full" data-aos="zoom-in-up">
        <div class="absolute top-0 inset-0 h-64 flex items-start">
            <div class="h-24 w-2/3 bg-gradient-to-br from-[#09C7FB] blur-2xl invisible opacity-40"></div>
            <div class="h-20 w-3/5 bg-gradient-to-r from-[#93FB9D] blur-2xl opacity-40"></div>
        </div>
        <div class="w-full px-5 sm:px-8 md:px-12 lg:py-64 max-w-screen-lg lg:max-w-screen-xl mx-auto relative">
            <div class="grid lg:grid-cols-2 gap-20 lx:gap-14 relative pt-24 lg:max-w-none max-w-2xl md:max-w-3xl mx-auto">
                <div class="lg:py-6">
                    <div class="text-center lg:text-left">
                        <h1 class="pt-4 text-white font-bold text-4xl md:text-5xl lg:text-6xl">
                            Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                                Bernard 
                            </span>
                            😎
                        </h1>
                    </div>
                    <p class="text-gray-300 pt-8 text-justify lg:text-justify mx-auto max-w-xl">
                            Welcome to my portfolio! I'm an aspiring web developer passionate about creating clean, 
                            functional, and visually appealing websites. With a foundation in HTML, CSS, JavaScript, 
                            and modern frameworks, I'm dedicated to continually learning and improving my skills to deliver 
                            seamless user experiences. I aim to build websites that not only look great but also perform smoothly 
                            across all devices.
                    </p>
                    <div class="flex items-center gap-3 pt-10 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0">
                        <button class="border border-green-500 border-solid px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center">
                            <div class="hover:scale-105 transition-all ease-in-out flex justify-center items-center relative">
                                <div class="svg-container">
                                    <DotLottieVue style="height: 30px; width: 30px" autoplay loop src="https://lottie.host/49017203-86b0-4565-beb7-920d6176bb7a/JR73wv2TOV.lottie" />
                                    <div class="download-loader text-white hidden"></div>
                                </div>
                                <a :href=resume download="BERNARD.pdf" class="pl-2 text-green-100"> Download Resume</a>
                            </div>
                        </button>
                        <div class="px-6 md:px-7 py3 relative group w-full sm:w-max flex justify-center ">
                            <!-- Social Media Icons -->
                            <a href="https://www.facebook.com/yej.eeb21/" rel="noopen norefferer" 
                            target="_blank" class="text-white hover:text-blue-500 px-3">
                                <Icon icon="fa6-brands:facebook" style="font-size: 3rem" />
                            </a>
                            <a href="https://www.instagram.com/itsme.jbee29/" 
                            rel="noopen norefferer" target="_blank" 
                            class="text-white hover:text-[#FF6F61] px-3">
                                <Icon icon="fa6-brands:instagram" style="font-size: 3rem" />
                            </a>
                            <a href="https://www.linkedin.com/in/bernard-arevalo-7903a9261/" 
                            rel="noopen norefferer" target="_blank" 
                            class="text-white hover:text-blue-400 px-3">
                                <Icon icon="fa6-brands:linkedin" style="font-size: 3rem" />
                            </a>
                            <a href="https://github.com/Jbee29" rel="noopen norefferer" target="_blank" 
                            class="text-white hover:text-gray-800 px-3">
                                <Icon icon="fa6-brands:github" style="font-size: 3rem" />
                            </a>
                        </div>
                    </div>
                </div>
                <div class="lg:h-full md:flex">
                    <div class="flex w-full h-96 min-h-[24rem] lg:min-h-[none] lg:w-full lg:h-full items-center relative justify-center">
                        <div class="absolute z-0 top-1/2 -translate-y-1/2 w-5/6 right-0 h-[calc(80%+20px)] bg-gradient-to-tr opacity-25 from-[#93FB9D] to-[#09C7FB] blur-2xl"></div>
                        <div class="absolute justify-center h-full z-10 p-2 -translate-y-1/2 top-1/2 lg:right-3 md:right-40 sm:right-16 rounded-full shadow border border-[#93FB9D]">
                            <img src="/src/assets/jb.jpeg" alt="my pic" width="400" height="400" loading="lazy" class="rounded-full h-full object-cover"/>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </Section>
</template>