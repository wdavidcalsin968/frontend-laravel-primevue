<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Dashboard
            </h2>
        </template>

        <div>
            <div
                class="bg-white min-h-screen overflow-hidden shadow-xl sm:rounded-lg p-4"
            >
                <!-- <Welcome /> -->
                <h2 class="uppercase text-3xl font-bold">
                    Bienvenidos a Dashboard
                </h2>
                <div class="text-black p-2">
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
