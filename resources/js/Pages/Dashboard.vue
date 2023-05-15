<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2
                class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight"
            >
                Dashboard
            </h2>
        </template>

        <div>
            <div
                class="bg-white dark:bg-gray-800 overflow-hidden shadow-xl sm:rounded-lg"
            >
                <Welcome />
                <div class="text-white p-2">
                    <h2>Count: {{ count }}</h2>
                    <button @click="count++" class="p-2 bg-blue-600">
                        increment
                    </button>
                    <button @click="count--" class="p-2 bg-blue-600">
                        decrement
                    </button>
                </div>

                <!-- <Button label="Check" icon="pi pi-check" /> -->
            </div>
        </div>
    </AppLayout>
</template>

<script>
export default {
    data() {
        return {
            count: 0,
        };
    },
};
</script>
