<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
import DataTable from "primevue/datatable";
import Column from "primevue/column";
import Button from "primevue/button";
import Dialog from "primevue/dialog";
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
                        <div class="text-gray-800 font-bold text-4xl text-center mb-2 leading-tight">USERS</div>
                        <p class="text-grey-darker text-base">Uso de Componentes</p>
                    </div>
                    </div>
                </div>
            </div>

            

            <div
                class="bg-white min-h-full overflow-hidden shadow-xl sm:rounded-lg p-4 flex flex-col border gap-8"
            >
            <h2
                class="py-2 text-3xl text-center font-bold text-gray-800"
            >
                Registrar y Editar Users
            </h2>
                
                <div class="flex justify gap-3">
                    <Button
                        icon="pi pi-users"
                        severity="success"
                        label="Registrar"
                    />
                
                </div>
                <div class="card">
                    <DataTable
                        :value="customers"
                        paginator
                        :rows="7"
                        :rowsPerPageOptions="[5, 10, 20, 50]"
                        tableStyle="min-width: 50rem"
                    >
                        <Column
                            field="name"
                            header="Name"
                            style="width: 25%"
                            sortable
                        ></Column>
                        <Column
                            field="country.name"
                            header="Country"
                            style="width: 25%"
                            sortable
                        ></Column>
                        <Column
                            field="company"
                            header="Company"
                            style="width: 25%"
                            sortable
                        ></Column>
                        <Column
                            field="representative.name"
                            header="Representative"
                            style="width: 25%"
                            sortable
                        ></Column>
                    </DataTable>
                </div>

                <!-- <Button label="Check" icon="pi pi-check" /> -->
            </div>
        </div>
    </AppLayout>
</template>

<script>
import { ref } from "vue";

const visible = ref(false);

export default {
    components: {
        Button,
    },
    data() {
        return {
            count: 0,
            customers: [
                {
                    name: "John Doe",
                    country: { name: "United States" },
                    company: "ABC Inc.",
                    representative: { name: "Jane Smith" },
                },
                {
                    name: "Alice Brown",
                    country: { name: "Canada" },
                    company: "XYZ Corp.",
                    representative: { name: "Bob Johnson" },
                },
                {
                    name: "John Doe",

                    country: { name: "United States" },

                    company: "ABC Inc.",

                    representative: { name: "Jane Smith" },
                },

                {
                    name: "Alice Brown",

                    country: { name: "Canada" },

                    company: "XYZ Corp.",

                    representative: { name: "Bob Johnson" },
                },

                {
                    name: "Mary Smith",

                    country: { name: "Australia" },

                    company: "DEF Corp.",

                    representative: { name: "John Adams" },
                },

                {
                    name: "David Lee",

                    country: { name: "South Korea" },

                    company: "GHI Inc.",

                    representative: { name: "Sarah Kim" },
                },

                {
                    name: "Juan Perez",

                    country: { name: "Mexico" },

                    company: "JKL Corp.",

                    representative: { name: "Maria Garcia" },
                },

                {
                    name: "Mohammed Ali",

                    country: { name: "Egypt" },

                    company: "MNO Inc.",

                    representative: { name: "Fatima Ahmed" },
                },

                {
                    name: "Hans Schmidt",

                    country: { name: "Germany" },

                    company: "PQR Corp.",

                    representative: { name: "Anna Mueller" },
                },

                {
                    name: "Yuki Nakamura",

                    country: { name: "Japan" },

                    company: "STU Inc.",

                    representative: { name: "Taro Yamada" },
                },

                {
                    name: "Maria Rodriguez",

                    country: { name: "Spain" },

                    company: "VWX Corp.",

                    representative: { name: "Carlos Sanchez" },
                },

                {
                    name: "Lena Svensson",

                    country: { name: "Sweden" },

                    company: "YZA Inc.",

                    representative: { name: "Erik Johansson" },
                },
            ],
        };
    },
    components: {
        DataTable,
    },
};
</script>
