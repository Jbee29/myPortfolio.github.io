<template>
    <div class="flex justify-center items-center h-full">
        <svg class="animate-spin h-16 w-16 text-white" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <defs>
                <linearGradient id="gradient1" x1="0%" x2="0%" y1="100%" y2="100%">
                    <stop offset="0%" stop-color="#93FB9D" />
                    <stop offset="100%" stop-color="#09C7FB" />
                </linearGradient>
            </defs>
            <circle class="opacity-25" cx="12" cy="12" r="10" stroke="url(#gradient1)" stroke-width="4" fill="none"></circle>
            <path fill="#93FB9D" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4z"></path>
        </svg>
    </div>
</template>