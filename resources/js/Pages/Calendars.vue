<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
import DataTable from "primevue/datatable";
import Calendar from "primevue/calendar";
import Column from "primevue/column";
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Datatable
            </h2>
        </template>

        <div>
            <div class="py-0 container max-w-full m-auto flex flex-wrap flex-col md:flex-row items-center justify-start">
                <div class="w-full lg:w-1/1 p-5">
                    <div class="flex flex-col lg:flex-row-reverse rounded overflow-hidden h-auto lg:h-32 border shadow-lg">
                    <img class="block h-auto w-full lg:w-44 flex-none bg-cover" src="/Sistemas.png">
                    <div class="bg-white rounded-b lg:rounded-b-none lg:rounded-r p-6 flex flex-col justify-between leading-normal">
                        <div class="text-gray-800 font-bold text-4xl text-center mb-2 leading-tight">CALENDARIO</div>
                        <p class="text-grey-darker text-base">Uso de Componentes</p>
                    </div>
                    </div>
                </div>
            </div>
            <div
                class="bg-white min-h-full overflow-hidden shadow-xl sm:rounded-lg p-4 flex flex-col border gap-8"
            >
                <h2
                    class="py-2 uppercase text-3xl text-center font-bold text-gray-800"
                >
                    Ingresar Calendario
                </h2>

                
                <div class="card flex gap-4 flex-wrap ">
                    <Calendar v-model="date1" dateFormat="dd/mm/yy" />
                    <Calendar v-model="date2" showIcon />
                    <Calendar
                        v-model="date3"
                        :minDate="minDate"
                        :maxDate="maxDate"
                        :manualInput="false"
                    />
                    <Calendar v-model="date4" inline showWeek />
                </div>

                <!-- <Button label="Check" icon="pi pi-check" /> -->
            </div>
        </div>
    </AppLayout>
</template>

<script>
import { ref } from "vue";

let today = new Date();
let month = today.getMonth();
let year = today.getFullYear();
let prevMonth = month === 0 ? 11 : month - 1;
let prevYear = prevMonth === 11 ? year - 1 : year;
let nextMonth = month === 11 ? 0 : month + 1;
let nextYear = nextMonth === 0 ? year + 1 : year;

const date1 = ref();
const date2 = ref();
const date3 = ref();
const date4 = ref();

const minDate = ref(new Date());
const maxDate = ref(new Date());

minDate.value.setMonth(prevMonth);
minDate.value.setFullYear(prevYear);
maxDate.value.setMonth(nextMonth);
maxDate.value.setFullYear(nextYear);

export default {
    components: {
        Calendar,
    },
};
</script>
