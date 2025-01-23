<script setup>
    import { ref } from 'vue';

    const education = ref([
        {
            id: 1,
            title: 'High School Diploma',
            school: 'Nation Muzon High School',
            year: '2004 - 2009',
        },
        {
            id: 2,
            title: 'Bachelor of Science in Information Technology',
            school: 'Bulacan State University',
            year: '2014 - 2018',
        },
    ]);
</script>

<template>
    <section class="text-white mt-8" id="about">
        <div class="absolute z-0 inset-x-0 h-64 flex items-start">
            <div class="h-20 w-80 bg-gradient-to-br from-[#93FB9D] via-[#09C7FB] blur-2xl to-[#99C7FB]"></div>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 lg:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white text-left mb-8">
                    My 
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                        Education
                    </span>
                </h2>
                <div class="space-y-12 py-0.5">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center md:w-[100%] w-full p-4 xl-rounded bg-[#111A3E] shadow-lg border border-[#1F1641]">
                        <div class="w-1/4 flex justify-center">
                            <img src="http://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png" alt="graduation-cap-icon" class="justify-center">
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB] lg:text-xl">
                                {{ element.school }}
                            </h3>
                            <p class="text-white"> {{ element.title }} </p>
                            <p class="text-white"> {{ element.year }} </p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-4 md:mt-0 text-left flex-col z-10 h-full" data-aos="flip-left">
                <h2 class="text-4xl font-bold text-white md:text-center text-left mb-4">
                    More About
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                        Me
                    </span>
                </h2>
                <p class="text-base lg:text-lg mt-2 py-2 text-justify">
                   Hi! I’m 33 years old and I hold a Bachelor of Science in Information Technology from Bulacan State University. 
                   I used to work as a Surveillance Operator, and now I’m excited to continue my education in the IT field. 
                   I’m eager to enhance my skills and keep up with all the latest advancements in the industry!
                </p>
                <h3 class="text-3xl font-bold text-white md:text-center text-left mb-4">
                    My 
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                        Hobbies
                    </span> 
                    are:
                </h3>
                <div class="grid grid-cols-3 gap-4 max-w-4xl pt-4">
                    <div class="text-center rounded-xl bg-[#111A3E] shadow-lg border border-[1F1641] p-3">
                        <p class="text-white font-bold text-xl sm:text-1xl lg:text-2xl">
                            Playing Basketball
                        </p>
                    </div>
                    <div class="text-center rounded-xl bg-[#111A3E] shadow-lg border border-[1F1641] p-3">
                        <p class="text-white font-bold text-xl sm:text-1xl lg:text-2xl">
                            Play Mobile Games
                        </p>
                    </div>
                    <div class="text-center rounded-xl bg-[#111A3E] shadow-lg border border-[1F1641] p-3">
                        <p class="text-white font-bold text-xl sm:text-1xl lg:text-2xl">
                            Reading Manga & Manhwa
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>