<script setup>
import { router } from "@inertiajs/vue3";
import { Link } from "@inertiajs/vue3";
import Menubar from "primevue/menubar";
import Button from "primevue/button";
import Sidebar from "primevue/sidebar";
import PanelMenu from "primevue/panelmenu";
import Avatar from "primevue/avatar";
import DropdownLink from "@/Components/DropdownLink.vue";

const logout = () => {
    router.post(route("logout"));
};
</script>

<template>
    <div class="bg-[#202A38] h-20 pl md:pl-72 fixed top-0 right-0 w-full">
        <div
            class="h-full w-full flex justify-between md:justify-end items-center px-4"
        >
            <div class="card block md:hidden">
                <Sidebar v-model:visible="visible">
                    <h2 class="text-center pb-8 text-xl font-bold">MENU</h2>
                    <PanelMenu :model="items" />
                </Sidebar>
                <Button icon="pi pi-align-left" @click="visible = true" />
            </div>
            <form @submit.prevent="logout">
                <Button label="Logout" icon="pi pi-sign-out" type="submit" />
            </form>
        </div>
    </div>
</template>

<script>
import { ref } from "vue";

const items = ref([
    {
        label: "File",
        icon: "pi pi-fw pi-file",
        items: [
            {
                label: "New",
                icon: "pi pi-fw pi-plus",
                items: [
                    {
                        label: "Bookmark",
                        icon: "pi pi-fw pi-bookmark",
                    },
                    {
                        label: "Video",
                        icon: "pi pi-fw pi-video",
                    },
                ],
            },
            {
                label: "Delete",
                icon: "pi pi-fw pi-trash",
            },
            {
                label: "Export",
                icon: "pi pi-fw pi-external-link",
            },
        ],
    },
    {
        label: "Edit",
        icon: "pi pi-fw pi-pencil",
        items: [
            {
                label: "Left",
                icon: "pi pi-fw pi-align-left",
            },
            {
                label: "Right",
                icon: "pi pi-fw pi-align-right",
            },
            {
                label: "Center",
                icon: "pi pi-fw pi-align-center",
            },
            {
                label: "Justify",
                icon: "pi pi-fw pi-align-justify",
            },
        ],
    },
    {
        label: "Users",
        icon: "pi pi-fw pi-user",
        items: [
            {
                label: "New",
                icon: "pi pi-fw pi-user-plus",
            },
            {
                label: "Delete",
                icon: "pi pi-fw pi-user-minus",
            },
            {
                label: "Search",
                icon: "pi pi-fw pi-users",
                items: [
                    {
                        label: "Filter",
                        icon: "pi pi-fw pi-filter",
                        items: [
                            {
                                label: "Print",
                                icon: "pi pi-fw pi-print",
                            },
                        ],
                    },
                    {
                        icon: "pi pi-fw pi-bars",
                        label: "List",
                    },
                ],
            },
        ],
    },
    {
        label: "Events",
        icon: "pi pi-fw pi-calendar",
        items: [
            {
                label: "Edit",
                icon: "pi pi-fw pi-pencil",
                items: [
                    {
                        label: "Save",
                        icon: "pi pi-fw pi-calendar-plus",
                    },
                    {
                        label: "Delete",
                        icon: "pi pi-fw pi-calendar-minus",
                    },
                ],
            },
            {
                label: "Archieve",
                icon: "pi pi-fw pi-calendar-times",
                items: [
                    {
                        label: "Remove",
                        icon: "pi pi-fw pi-calendar-minus",
                    },
                ],
            },
        ],
    },
]);

const visible = ref(false);

export default {
    components: {
        Menubar,
        Button,
        Sidebar,
        PanelMenu,
    },
};
</script>
