<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
import DataTable from "primevue/datatable";
import Column from "primevue/column";
import Button from "primevue/button";
import InputText from 'primevue/inputtext';
import AutoComplete from 'primevue/autocomplete';
import Calendar from 'primevue/calendar';
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Formulario
            </h2>
        </template>

        <div>
            <div
                class="bg-white min-h-screen overflow-hidden shadow-xl sm:rounded-lg p-4 flex flex-col gap-8"
            >
                <!-- <Welcome /> -->
                <h2 class="uppercase text-3xl text-center font-bold text-gray-800">
                    Formulario
                </h2>
                
                <h:form>
                    <div class="flex flex-col gap-6">
                        <div class=" flex flex-wrap -mx-3 mb-2 ">       
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto ">
                                    <span class="p-float-label">
                                        <InputText class="appearance-none block w-full bg-white-200 text-gray-700 border border-black-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" id="username" v-model="value" />
                                        <label for="username">Nombres</label>
                                    </span>
                                </div>
                                
                            </div>
                            <div class=" w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto ">
                                    <span class="p-float-label">
                                        <InputText class="appearance-none block w-full bg-white-200 text-gray-700 border border-black-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" id="username" v-model="value" />
                                        <label for="username">Apellido Paterno</label>
                                    </span>
                                </div>
                                
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto">
                                    <span class="p-float-label">
                                        <InputText class="appearance-none block w-full bg-white-200 text-gray-700 border border-black-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" id="username" v-model="value" />
                                        <label for="username">Apellido Materno</label>
                                    </span>
                                </div>
                            </div>
                        </div>

                        <div class=" flex flex-wrap -mx-3 mb-2 ">       
                            <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto ">
                                    <span class="p-float-label">
                                        <InputText class="appearance-none block w-full bg-white-200 text-gray-700 border border-black-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" id="username" v-model="value" />
                                        <label for="username">Correo Electronico</label>
                                    </span>
                                </div>
                                
                            </div>
                            <div class=" w-full md:w-1/2 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto ">
                                    <span class="p-float-label">
                                        <InputText class="appearance-none block w-full bg-white-200 text-gray-700 border border-black-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" id="username" v-model="value" />
                                        <label for="username">N° Celular o Telefono</label>
                                    </span>
                                </div>
                                
                            </div>
                        </div>

                        <div class=" flex flex-wrap -mx-3 mb-2 ">       
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto ">
                                    <span class="p-float-label">
                                        <AutoComplete class="w-full" v-model="value" dropdown :suggestions="items" @complete="search" />
                                        <label for="username">Seleccione</label>
                                    </span>
                                </div>
                                
                            </div>
                            <div class=" w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto ">
                                    <span class="p-float-label">
                                        <Calendar class="w-full" v-model="date2" showIcon />
                                    </span>
                                </div>
                                
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class=" flex-auto">
                                    <span class="p-float-label">
                                        <InputText class="appearance-none block w-full bg-white-200 text-gray-700 border border-black-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" id="username" v-model="value" />
                                        <label for="username">DNI</label>
                                    </span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="flex flex-col gap-6 ">
                            <div class="flex flex-col md:w-1/3 py-10">
                                <Button
                                    label="Guardar"
                                    severity="success"
                                    type="submit"
                                />
                            </div>
                        </div>
                </h:form>

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

const date2 = ref();

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
    components: {
        Button,
        InputText,
    },
};

</script>
