<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import Welcome from "@/Components/Welcome.vue";
import DataTable from "primevue/datatable";
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
            <div
                class="bg-white min-h-screen overflow-hidden shadow-xl sm:rounded-lg p-4 flex flex-col gap-8"
            >
                <!-- <Welcome /> -->
                <h2 class="uppercase text-3xl font-bold text-gray-800">
                    Bienvenidos a Calendarios
                </h2>
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
                        ></Column>
                        <Column
                            field="country.name"
                            header="Country"
                            style="width: 25%"
                        ></Column>
                        <Column
                            field="company"
                            header="Company"
                            style="width: 25%"
                        ></Column>
                        <Column
                            field="representative.name"
                            header="Representative"
                            style="width: 25%"
                        ></Column>
                    </DataTable>
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
