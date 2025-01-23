<script>
    import Swal from 'sweetalert2';
    // This is a free script from Wen3from.com
    const WEB3FORMS_ACCESS_KEY = "eb29e053-a13a-4fdf-9b66-7d53c0d7e883";
    // const Swal = require('sweetalert2');

        export default {
            data() {
                return {
                    email: "",
                    subject: "",
                    message: "",
                };
            },
            methods: {
                async submitForm() {
                    const response = await fetch("https://api.web3forms.com/submit", {
                        method: "POST",
                        headers: {
                            "Content-Type": "application/json",
                            Accept: "application/json",
                        },
                        body: JSON.stringify({
                            access_key: WEB3FORMS_ACCESS_KEY,
                            email: this.email,
                            subject: this.subject,
                            message: this.message,
                        }),
                    });
                    const result = await response.json();
                    if (result.success) {
                        console.log(result);
                        Swal.fire({
                        title: "Success!",
                        text: "Message Sent Successfully!",
                        icon: "success"
                        });
                        email.value = '';
                        subject.value = '';
                        message.value = '';
                    }
                },
            },
        };
</script>

<template>
    <section class="text-white mt-64" id="contact">
        <h2 class="text-4xl font-bold uppercase text-white text-left mb-4 px-4 xl:pl-16"> 
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#93FB9D] to-[#09C7FB]">
                    Let's talk
             </span>
        </h2>
        <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
            <div>
                <p class="text-white">
                    Here's are my contact details:
                </p>
                <div class="col-lg-4 col-md-4mb-lg-0 mt-5"></div>
                <div class="flex mb-10 items-center">
                    <div class="p-2"
                    style="background: #111A3E; width: 50px; height: 48px; display: flex; justify-content: center; border-radius: 50%;
                    overflow: hidden; border: 1px solid #111A3E; backdrop-filter: blur(9px); -webkit-backdrop-filter: blur(9px);">
                        <img src="https://img.icons8.com/metro/50/ffffff/new-post.png" alt="new-post" class="w-6">
                    </div>
                    <div class="ml-5 text-white">
                        <h4>Email</h4>
                        <p>bernard.arevalo29@gmail.com</p>
                    </div>
                </div>
                <div class="flex mb-10 items-center">
                    <div class="p-2"
                    style="background: #111A3E; width: 50px; height: 48px; display: flex; justify-content: center; border-radius: 50%;
                    overflow: hidden; border: 1px solid #111A3E; backdrop-filter: blur(9px); -webkit-backdrop-filter: blur(9px);">
                        <img src="https://img.icons8.com/ios-filled/50/ffffff/phone.png" alt="phone" class="w-6">
                    </div>
                    <div class="ml-5 text-white">
                        <h4>Phone</h4>
                        <p>+63-9354-7777-586</p>
                    </div>
                </div>
                <div class="flex mb-10 items-center">
                    <div class="p-2"
                    style="background: #111A3E; width: 50px; height: 48px; display: flex; justify-content: center; border-radius: 50%;
                    overflow: hidden; border: 1px solid #111A3E; backdrop-filter: blur(9px); -webkit-backdrop-filter: blur(9px);">
                        <img src="https://img.icons8.com/ios-filled/50/ffffff/linkedin.png" alt="linkedin" class="w-6">
                    </div>
                    <div class="ml-5 text-white">
                        <h4>LinkedIn</h4>
                        <p>https://www.linkedin.com/in/bernard-arevalo-7903a9261/bernard.arevalo29@gmail.com</p>
                    </div>
                </div>
            </div>
            <div style="background: #111A3E; width: 100%; height: 100%; border-radius: 15px;
            overflow: hidden; border: 1px solid #111A3E; backdrop-filter: blur(9px); -webkit-backdrop-filter: blur(9px);">
                <form class="flex flex-col p-2" @submit.prevent="submitForm" data-aos="zoom-in-up">
                    <div class="mb-6">
                        <label for="email" class="text-white block mb-2 text-sm font-medium">Email</label>
                        <input type="email" id="email" v-model="email" name="email" 
                        class="bg-[#111827] placeholder-[#9CA2A9] text-white text-sm rounded-lg block w-full p-2.5" 
                        placeholder="Email@xxxx.com" required>
                    </div>
                    <div class="mb-6">
                        <label for="subject" class="text-white block mb-2 text-sm font-medium">Subject</label>
                        <input type="text" id="subject" v-model="subject" name="subject" 
                        class="bg-[#111827] placeholder-[#9CA2A9] text-white text-sm rounded-lg block w-full p-2.5" 
                        placeholder="Subject" required>
                    </div>
                    <div class="mb-6">
                        <label for="message" class="text-white block mb-2 text-sm font-medium">Message</label>
                        <textarea id="message" name="message" v-model="message" 
                        class="bg-[#111827] placeholder-[#9CA2A9] text-white text-sm rounded-lg block w-full p-2.5" 
                        placeholder="Message here..." required></textarea>
                    </div>
                    <button class="z-1 w-[100%!important] px-6 md:px-7 py-3 rounded-full sm:w-max flex justify-center text-black bg-green-600 
                    hover:bg-gradient-to-r from-[#93FB9D] to-[#09C7FB] border border-transparent" type="submit">
                        Send Message
                    </button>
                </form>
            </div>
            <div class="bg-gradient-to-r from-[#93FB9D] via-[#09C7FB] to-[#09C7FB] blur-2xl h-20 w-80 z-0 absolute -top-1/2 -left-4 transform -translate-x-2/3 -translate-1/2"></div>
        </div>
    </section>
</template>