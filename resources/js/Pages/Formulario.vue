<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
import Button from "primevue/button";
import InputText from "primevue/inputtext";
import AutoComplete from "primevue/autocomplete";
import Calendar from "primevue/calendar";
import Password from "primevue/password";
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
                <h2
                    class="uppercase text-3xl text-center font-bold text-gray-800"
                >
                    Formulario
                </h2>

                <div class="pb-6 relative flex py-0 items-center">
                    <div class="flex-grow border-t border-gray-400"></div>
                    <span class="flex-shrink mx-4 text-gray-400"
                        >Llenar el formulario correctamente</span
                    >
                    <div class="flex-grow border-t border-gray-400"></div>
                </div>

                <h:form>
                    <div class="flex flex-col gap-10">
                        <div class="flex flex-wrap">
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <InputText
                                            class="w-full"
                                            id="username"
                                            v-model="value"
                                        />
                                        <label for="username">Nombres</label>
                                    </span>
                                </div>
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <InputText
                                            class="w-full"
                                            id="username"
                                            v-model="value"
                                        />

                                        <label for="username"
                                            >Apellido Paterno</label
                                        >
                                    </span>
                                </div>
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <InputText
                                            class="w-full"
                                            id="username"
                                            v-model="value"
                                        />
                                        <label for="username"
                                            >Apellido Materno</label
                                        >
                                    </span>
                                </div>
                            </div>
                        </div>

                        <div class="flex flex-wrap">
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <InputText
                                            class="w-full"
                                            id="username"
                                            v-model="value"
                                        />
                                        <label for="username">DNI</label>
                                    </span>
                                </div>
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <InputText
                                            class="w-full"
                                            id="username"
                                            v-model="value"
                                            type="email"
                                            placeholder="example@example.com"
                                        />
                                        <label for="username"
                                            >Correo Electronico</label
                                        >
                                    </span>
                                </div>
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <InputText
                                            class="w-full"
                                            id="username"
                                            v-model="value"
                                            type="number"
                                        />
                                        <label for="username"
                                            >N° Celular o Telefono</label
                                        >
                                    </span>
                                </div>
                            </div>
                        </div>

                        <div class="flex flex-wrap">
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <InputText
                                            class="w-full"
                                            id="username"
                                            v-model="value"
                                        />
                                        <label for="username"
                                            >Descripción</label
                                        >
                                    </span>
                                </div>
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <!-- <AutoComplete
                                            class="w-full"
                                            v-model="selectedItem"
                                            dropdown
                                            :suggestions="filteredItems"
                                            @complete="searchItems"
                                        /> -->
                                        <AutoComplete
                                            class="w-full"
                                            v-model="selectedItem"
                                            :suggestions="filteredItems"
                                            @complete="searchItems"
                                            :virtualScrollerOptions="{
                                                itemSize: 38,
                                            }"
                                            optionLabel="label"
                                            dropdown
                                        />
                                        <label for="username">Seleccione</label>
                                    </span>
                                </div>
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <div class="flex-auto">
                                    <span class="p-float-label">
                                        <Calendar
                                            class="w-full"
                                            v-model="date2"
                                            showIcon
                                        />
                                    </span>
                                </div>
                            </div>
                        </div>

                        <div class="flex flex-wrap w-full">
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <span class="p-float-label w-full">
                                    <Password
                                        class="w-full"
                                        v-model="value"
                                        inputId="password"
                                        input-class="w-full"
                                        toggleMask
                                    />
                                    <label for="password">Password</label>
                                </span>
                            </div>
                            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                                <span class="p-float-label">
                                    <Password
                                        class="w-full"
                                        v-model="value"
                                        inputId="password"
                                        toggleMask
                                        input-class="w-full"
                                    />
                                    <label for="password"
                                        >Confirm Password</label
                                    >
                                </span>
                            </div>
                        </div>
                    </div>

                    <div class="flex flex-col gap-6">
                        <div class="flex flex-col items-center py-10">
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

const countries = ["Peru", "Colombia", "Ecuador", "Argentina"];

const items = ref(
    Array.from({ length: countries.length }, (_, i) => ({
        label: countries[i],
        value: i,
    }))
);
const selectedItem = ref();
const filteredItems = ref();
const searchItems = (event) => {
    let query = event.query;
    let _filteredItems = [];

    for (let i = 0; i < items.value.length; i++) {
        let item = items.value[i];

        if (item.label.toLowerCase().indexOf(query.toLowerCase()) === 0) {
            _filteredItems.push(item);
        }
    }

    filteredItems.value = _filteredItems;
};
</script>
