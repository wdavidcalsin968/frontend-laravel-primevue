<script setup>
import { Head, Link, router } from "@inertiajs/vue3";

import Banner from "@/Components/Banner.vue";

import NabvarDashboard from "../ComponentsDashboard/NabvarDashboard.vue";
import SidebarDashboard from "../ComponentsDashboard/SidebarDashboard.vue";
</script>

<template>
    <div>
        <Head :title="title" />

        <Banner />

        <div class="min-h-screen bg-gray-100 dark:bg-gray-900 rounded-0">
            <NabvarDashboard />
            <SidebarDashboard />
            <main class="bg-red-500 pl-0 md:pl-72 pt-20">
                <div class="p-3">
                    <slot />
                </div>
            </main>
        </div>
    </div>
</template>
