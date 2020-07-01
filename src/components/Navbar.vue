<template>
    <nav class="flex-col bg-blue-700 p-3 h-full">
        <div>
            <span class="mx-5 text-white text-3xl">
                <i class="fas fa-book"></i>
                <span>
                    Readr
                </span>
            </span>
        </div>
        <router-link
                to="/"
                v-slot="{ isExactActive, navigate }"
            >
            <div class="mt-12 rounded-md text-left px-8 py-2" :class="isExactActive ? 'bg-blue-800' : 'hover:bg-blue-600'" @click="navigate">
                <span class="text-white text-2xl">
                    List
                </span>
            </div>
        </router-link>
        <router-link
            to="/log"
            v-slot="{ isActive, navigate }"
        >
            <div class="mt-5 rounded-md text-left px-8 py-2" :class="isActive ? 'bg-blue-800' : 'hover:bg-blue-600'" @click="navigate">
                <span class="text-white text-2xl">
                    Log
                </span>
            </div>
        </router-link>
        <router-link
            to="/explore"
            v-slot="{ isActive, navigate }"
        >
            <div class="mt-5 rounded-md text-left px-8 py-2" :class="isActive ? 'bg-blue-800' : 'hover:bg-blue-600'" @click="navigate">
                <span class="text-white text-2xl">
                    Explore
                </span>
            </div>
        </router-link>
    </nav>
</template>