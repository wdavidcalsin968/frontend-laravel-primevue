<script setup>
import PanelMenu from "primevue/panelmenu";
</script>

<template>
    <div
        class="w-72 bg-[#202A38] h-screen px-1 fixed top-0 left-0 hidden md:block border-r-[1px] border-gray-700 text-white overflow-auto"
    >
        <h2 class="text-center py-8 text-xl font-bold">MENU</h2>
        <PanelMenu
            v-model:expandedKeys="expandedKeys"
            :model="items"
            class="bg-[#111827] p-3 border-gray-300 rounded-md"
        >
            <template #header>
                <i class="pi pi-fw pi-file"></i>
                <span class="font-bold">Opción 1</span>
            </template>
            <template #model>
                <PanelMenuItem :label="'Subopción 1'" />
                <PanelMenuItem :label="'Subopción 2'" />
            </template>
        </PanelMenu>
    </div>
</template>

<script>
import { ref } from "vue";

const expandedKeys = ref({});
const items = ref([
    {
        key: "0",
        label: "File",
        icon: "pi pi-fw pi-file",
        items: [
            {
                key: "0_0",
                label: "New",
                icon: "pi pi-fw pi-plus",
                items: [
                    {
                        key: "0_0_0",
                        label: "Bookmark",
                        icon: "pi pi-fw pi-bookmark",
                    },
                    {
                        key: "0_0_1",
                        label: "Video",
                        icon: "pi pi-fw pi-video",
                    },
                ],
            },
            {
                key: "0_1",
                label: "Delete",
                icon: "pi pi-fw pi-trash",
            },
            {
                key: "0_2",
                label: "Export",
                icon: "pi pi-fw pi-external-link",
            },
        ],
    },
    {
        key: "1",
        label: "Edit",
        icon: "pi pi-fw pi-pencil",
        items: [
            {
                key: "1_0",
                label: "Left",
                icon: "pi pi-fw pi-align-left",
            },
            {
                key: "1_1",
                label: "Right",
                icon: "pi pi-fw pi-align-right",
            },
            {
                key: "1_2",
                label: "Center",
                icon: "pi pi-fw pi-align-center",
            },
            {
                key: "1_3",
                label: "Justify",
                icon: "pi pi-fw pi-align-justify",
            },
        ],
    },
    {
        key: "2",
        label: "Users",
        icon: "pi pi-fw pi-user",
        items: [
            {
                key: "2_0",
                label: "New",
                icon: "pi pi-fw pi-user-plus",
            },
            {
                key: "2_1",
                label: "Delete",
                icon: "pi pi-fw pi-user-minus",
            },
            {
                key: "2_2",
                label: "Search",
                icon: "pi pi-fw pi-users",
                items: [
                    {
                        key: "2_2_0",
                        label: "Filter",
                        icon: "pi pi-fw pi-filter",
                        items: [
                            {
                                key: "2_2_0_0",
                                label: "Print",
                                icon: "pi pi-fw pi-print",
                            },
                        ],
                    },
                    {
                        key: "2_2_1",
                        icon: "pi pi-fw pi-bars",
                        label: "List",
                    },
                ],
            },
        ],
    },
    {
        key: "3",
        label: "Events",
        icon: "pi pi-fw pi-calendar",
        items: [
            {
                key: "3_0",
                label: "Edit",
                icon: "pi pi-fw pi-pencil",
                items: [
                    {
                        key: "3_0_0",
                        label: "Save",
                        icon: "pi pi-fw pi-calendar-plus",
                    },
                    {
                        key: "3_0_0",
                        label: "Delete",
                        icon: "pi pi-fw pi-calendar-minus",
                    },
                ],
            },
            {
                key: "3_1",
                label: "Archieve",
                icon: "pi pi-fw pi-calendar-times",
                items: [
                    {
                        key: "3_1_0",
                        label: "Remove",
                        icon: "pi pi-fw pi-calendar-minus",
                    },
                ],
            },
        ],
    },
]);

const expandAll = () => {
    for (let node of items.value) {
        expandNode(node);
    }

    expandedKeys.value = { ...expandedKeys.value };
};

const collapseAll = () => {
    expandedKeys.value = {};
};

const expandNode = (node) => {
    if (node.items && node.items.length) {
        expandedKeys.value[node.key] = true;

        for (let child of node.items) {
            expandNode(child);
        }
    }
};

export default {
    components: {
        PanelMenu,
    },
};
</script>
