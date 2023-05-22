<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
import Chart from "primevue/chart";

defineProps({ user: Array });
</script>

<template>
    <AppLayout title="Dashboard" userName="{{user.name}}">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Dashboard
            </h2>
        </template>

        <div>
            <div
                class="bg-white min-h-screen overflow-hidden shadow-xl sm:rounded-lg p-4 flex flex-col gap-7"
            >
                <!-- <Welcome /> -->
                <h2 class="uppercase text-3xl text-center font-bold">
                    Bienvenidos al sistema 
                    <span class="font-bold uppercase">{{
                        $page.props.auth.user.name
                    }}</span>
                </h2>
                <div class="pb-6 relative flex py-0 items-center">
                    <div class="flex-grow border-t border-gray-400"></div>
                        <span class="flex-shrink mx-4 text-gray-400">Ingenieria de Sistemas</span>
                    <div class="flex-grow border-t border-gray-400"></div>
                </div>
                <div class="flex gap-4">
                    <Chart
                        type="bar"
                        :data="chartData"
                        :options="chartOptions"
                        class="flex-1"
                    />
                    <Chart
                        type="pie"
                        :data="chartData"
                        :options="chartOptions"
                        class="flex-1 w-full md:w-30rem"
                    />
                </div>
                <div class="text-black p-2">
                    <h2 class="uppercase font-bold">Count: {{ count }}</h2>
                    <div class="flex gap-3">
                        <button
                            @click="count++"
                            class="p-2 bg-blue-600 rounded-md text-white"
                        >
                            increment
                        </button>
                        <button
                            @click="count--"
                            class="p-2 bg-blue-600 rounded-md text-white"
                        >
                            decrement
                        </button>
                    </div>
                </div>

                <!-- <Button label="Check" icon="pi pi-check" /> -->
            </div>
        </div>
    </AppLayout>
</template>

<script>
import { ref } from "vue";

const chartData = ref({
    labels: ["Q1", "Q2", "Q3", "Q4"],
    datasets: [
        {
            label: "Sales",
            data: [540, 325, 702, 620],
            backgroundColor: [
                "rgba(255, 159, 64, 0.2)",
                "rgba(75, 192, 192, 0.2)",
                "rgba(54, 162, 235, 0.2)",
                "rgba(153, 102, 255, 0.2)",
            ],
            borderColor: [
                "rgb(255, 159, 64)",
                "rgb(75, 192, 192)",
                "rgb(54, 162, 235)",
                "rgb(153, 102, 255)",
            ],
            borderWidth: 1,
        },
    ],
});
const chartOptions = ref({
    scales: {
        y: {
            beginAtZero: true,
        },
    },
});

export default {
    components: {
        Chart,
    },
    data() {
        return {
            count: 0,
        };
    },
};
</script>
