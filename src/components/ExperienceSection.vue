<script setup>
    import { ref } from 'vue';

    const experience = ref([
        {
            id: 1,
            title: 'CCTV Operator',
            company: 'Paramount Human Resource Multi-Purpose Cooperative',
            year: '2018 - 2024',
            description: 'I was responsible for monitoring the surveillance cameras and ensuring the safety and security of the Northstar Meat Mechandise Inc. premises. I also maintained a log of all activities and incidents that occurred during my shift.',
            duties: ['Monitor surveillance cameras', 'Maintain log of activities and incidents', 'Ensure safety and security of premises', 'Report any suspicious activities to my supervisor',
            'Coordinate with law enforcement agencies when necessary', 'Assist in investigations when needed', 'Provide support to other security personnel as needed', 'Perform other duties as troubleshooting and maintenance of equipment'],
        },
    ]);
</script>

<template>
    <section class="text-white mt-18" id="experience">
        <div data-aos="zoom-in" class="items-center py-8 px-4 lg:gap-16 sm:py-16 xl:px-16 z-1">
            <h2 class="text-4xl font-bold text-white mb-8 md:text-center md:mt-0 mt-8">
                My 
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                    Experience
                </span>
            </h2>
            <div class="space-y-8 py-8">
                <div v-for="element in experience" :key="element.id" 
                class="flex items-center md:w-[100%] w-full rounded-xl p-4 bg-[#111A3E] shadow-lg border border-[#1F1641]">
                    <div class="w-1/4 flex justify-center">
                        <img src="http://img.icons8.com/ios-filled/100/ffffff/lawyer.png" alt="lawyer" class="w-1/2">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                            {{ element.title }}
                        </h3>
                        <p class="text-white"> {{ element.company }} </p>
                        <p class="text-white"> {{ element.year }} </p>
                        <p class="text-white"> {{ element.description }} </p>
                        <p class="text-white pt-4 font-semibold uppercase"> Responsibilities </p>
                        <div v-for="responsibilities in element.duties" :key="responsibilities">
                            <li class="text-white"> {{ responsibilities }} </li>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>