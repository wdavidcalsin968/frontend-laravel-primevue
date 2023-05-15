<script setup>
import { router } from "@inertiajs/vue3";
import { Link } from "@inertiajs/vue3";
import Menubar from "primevue/menubar";
import Button from "primevue/button";
import Sidebar from "primevue/sidebar";
import PanelMenu from "primevue/panelmenu";
import Menu from "primevue/menu";
import Avatar from "primevue/avatar";
import DropdownLink from "@/Components/DropdownLink.vue";

const logout = () => {
    router.post(route("logout"));
};
</script>

<template>
    <div class="bg-[#0F172A] h-16 pl md:pl-72 fixed top-0 right-0 w-full z-40">
        <div
            class="h-full w-full flex justify-between md:justify-end items-center px-4"
        >
            <div class="card block md:hidden">
                <Sidebar class="bg-white" v-model:visible="visible">
                    <!-- <h2 class="text-center pb-8 text-xl font-bold">MENU</h2>
                    <PanelMenu :model="items" /> -->
                    <div
                        class="w-full h-full py-4 overflow-y-auto bg-white px-3 flex flex-col gap-10"
                    >
                        <!-- <div
                            class="flex justify-between items-center mt-3 px-3"
                        >
                            <img class="w-8" src="/logo_unap.png" alt="" />
                            <div
                                class="relative cursor-pointer hover:bg-white/10 p-2 rounded-full"
                            >
                                <svg
                                    aria-hidden="true"
                                    class="w-7 h-7  transition duration-75 dark:  dark:group-hover:text-white"
                                    fill="currentColor"
                                    xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 448 512"
                                >
                                    
                                    <path
                                        d="M224 0c-17.7 0-32 14.3-32 32V49.9C119.5 61.4 64 124.2 64 200v33.4c0 45.4-15.5 89.5-43.8 124.9L5.3 377c-5.8 7.2-6.9 17.1-2.9 25.4S14.8 416 24 416H424c9.2 0 17.6-5.3 21.6-13.6s2.9-18.2-2.9-25.4l-14.9-18.6C399.5 322.9 384 278.8 384 233.4V200c0-75.8-55.5-138.6-128-150.1V32c0-17.7-14.3-32-32-32zm0 96h8c57.4 0 104 46.6 104 104v33.4c0 47.9 13.9 94.6 39.7 134.6H72.3C98.1 328 112 281.3 112 233.4V200c0-57.4 46.6-104 104-104h8zm64 352H224 160c0 17 6.7 33.3 18.7 45.3s28.3 18.7 45.3 18.7s33.3-6.7 45.3-18.7s18.7-28.3 18.7-45.3z"
                                    />
                                </svg>

                                <span
                                    class="bg-green-500 w-5 p-1 text-white text-center font-bold text-[0.5rem] absolute top-1 right-0 rounded-full"
                                >
                                    2
                                </span>
                            </div>
                        </div> -->

                        <div class="flex flex-col gap-4">
                            <div class="ml-4 leading-4">
                                <h2 class="text-[#818CF8] font-bold">
                                    Dashboards
                                </h2>
                                <span class="text-[#878B95] text-xs"
                                    >Unico diseño de dashboard
                                </span>
                            </div>

                            <ul class="space-y-1.5 font-medium">
                                <li>
                                    <Link
                                        href="/dashboard"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-md bg-white/10 hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-6 h-6 transition duration-75 group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 576 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M575.8 255.5c0 18-15 32.1-32 32.1h-32l.7 160.2c0 2.7-.2 5.4-.5 8.1V472c0 22.1-17.9 40-40 40H456c-1.1 0-2.2 0-3.3-.1c-1.4 .1-2.8 .1-4.2 .1H416 392c-22.1 0-40-17.9-40-40V448 384c0-17.7-14.3-32-32-32H256c-17.7 0-32 14.3-32 32v64 24c0 22.1-17.9 40-40 40H160 128.1c-1.5 0-3-.1-4.5-.2c-1.2 .1-2.4 .2-3.6 .2H104c-22.1 0-40-17.9-40-40V360c0-.9 0-1.9 .1-2.8V287.6H32c-18 0-32-14-32-32.1c0-9 3-17 10-24L266.4 8c7-7 15-8 22-8s15 2 21 7L564.8 231.5c8 7 12 15 11 24z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Inicio</span
                                            >
                                        </div>
                                    </Link>
                                </li>

                                <li>
                                    <Link
                                        href="/datatable"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-lg hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-7 h-7 transition duration-75 dark:group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 512 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M64 256V160H224v96H64zm0 64H224v96H64V320zm224 96V320H448v96H288zM448 256H288V160H448v96zM64 32C28.7 32 0 60.7 0 96V416c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V96c0-35.3-28.7-64-64-64H64z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Datatable</span
                                            >
                                        </div>
                                    </Link>
                                </li>
                                <li>
                                    <Link
                                        href="/calendars"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-lg hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-7 h-7 transition duration-75 dark:group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 448 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M96 32V64H48C21.5 64 0 85.5 0 112v48H448V112c0-26.5-21.5-48-48-48H352V32c0-17.7-14.3-32-32-32s-32 14.3-32 32V64H160V32c0-17.7-14.3-32-32-32S96 14.3 96 32zM448 192H0V464c0 26.5 21.5 48 48 48H400c26.5 0 48-21.5 48-48V192z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Calendars</span
                                            >
                                        </div>
                                    </Link>
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-lg hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-6 h-6 transition duration-75 group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 512 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M441 58.9L453.1 71c9.4 9.4 9.4 24.6 0 33.9L424 134.1 377.9 88 407 58.9c9.4-9.4 24.6-9.4 33.9 0zM209.8 256.2L344 121.9 390.1 168 255.8 302.2c-2.9 2.9-6.5 5-10.4 6.1l-58.5 16.7 16.7-58.5c1.1-3.9 3.2-7.5 6.1-10.4zM373.1 25L175.8 222.2c-8.7 8.7-15 19.4-18.3 31.1l-28.6 100c-2.4 8.4-.1 17.4 6.1 23.6s15.2 8.5 23.6 6.1l100-28.6c11.8-3.4 22.5-9.7 31.1-18.3L487 138.9c28.1-28.1 28.1-73.7 0-101.8L474.9 25C446.8-3.1 401.2-3.1 373.1 25zM88 64C39.4 64 0 103.4 0 152V424c0 48.6 39.4 88 88 88H360c48.6 0 88-39.4 88-88V312c0-13.3-10.7-24-24-24s-24 10.7-24 24V424c0 22.1-17.9 40-40 40H88c-22.1 0-40-17.9-40-40V152c0-22.1 17.9-40 40-40H200c13.3 0 24-10.7 24-24s-10.7-24-24-24H88z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Registrar Usuario</span
                                            >
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-lg hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-6 h-6 transition duration-75 group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 640 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M144 0a80 80 0 1 1 0 160A80 80 0 1 1 144 0zM512 0a80 80 0 1 1 0 160A80 80 0 1 1 512 0zM0 298.7C0 239.8 47.8 192 106.7 192h42.7c15.9 0 31 3.5 44.6 9.7c-1.3 7.2-1.9 14.7-1.9 22.3c0 38.2 16.8 72.5 43.3 96c-.2 0-.4 0-.7 0H21.3C9.6 320 0 310.4 0 298.7zM405.3 320c-.2 0-.4 0-.7 0c26.6-23.5 43.3-57.8 43.3-96c0-7.6-.7-15-1.9-22.3c13.6-6.3 28.7-9.7 44.6-9.7h42.7C592.2 192 640 239.8 640 298.7c0 11.8-9.6 21.3-21.3 21.3H405.3zM224 224a96 96 0 1 1 192 0 96 96 0 1 1 -192 0zM128 485.3C128 411.7 187.7 352 261.3 352H378.7C452.3 352 512 411.7 512 485.3c0 14.7-11.9 26.7-26.7 26.7H154.7c-14.7 0-26.7-11.9-26.7-26.7z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Usuarios</span
                                            >
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-lg hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-6 h-6 transition duration-75 group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 576 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M0 64C0 28.7 28.7 0 64 0H224V128c0 17.7 14.3 32 32 32H384V285.7l-86.8 86.8c-10.3 10.3-17.5 23.1-21 37.2l-18.7 74.9c-2.3 9.2-1.8 18.8 1.3 27.5H64c-35.3 0-64-28.7-64-64V64zm384 64H256V0L384 128zM549.8 235.7l14.4 14.4c15.6 15.6 15.6 40.9 0 56.6l-29.4 29.4-71-71 29.4-29.4c15.6-15.6 40.9-15.6 56.6 0zM311.9 417L441.1 287.8l71 71L382.9 487.9c-4.1 4.1-9.2 7-14.9 8.4l-60.1 15c-5.5 1.4-11.2-.2-15.2-4.2s-5.6-9.7-4.2-15.2l15-60.1c1.4-5.6 4.3-10.8 8.4-14.9z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Formulario</span
                                            >
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-lg hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-6 h-6 transition duration-75 group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 384 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M64 0C28.7 0 0 28.7 0 64V448c0 35.3 28.7 64 64 64H320c35.3 0 64-28.7 64-64V160H256c-17.7 0-32-14.3-32-32V0H64zM256 0V128H384L256 0zM216 232V334.1l31-31c9.4-9.4 24.6-9.4 33.9 0s9.4 24.6 0 33.9l-72 72c-9.4 9.4-24.6 9.4-33.9 0l-72-72c-9.4-9.4-9.4-24.6 0-33.9s24.6-9.4 33.9 0l31 31V232c0-13.3 10.7-24 24-24s24 10.7 24 24z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Reporte</span
                                            >
                                        </div>
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="flex flex-col gap-4">
                            <div class="ml-4 leading-4">
                                <h2 class="text-[#818CF8] font-bold">
                                    Aplicaciones
                                </h2>
                                <span class="text-[#878B95] text-xs"
                                    >Customizacion de componentes</span
                                >
                            </div>

                            <ul class="space-y-1.5 font-medium">
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-md hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-6 h-6 transition duration-75 group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 640 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M320 32c-8.1 0-16.1 1.4-23.7 4.1L15.8 137.4C6.3 140.9 0 149.9 0 160s6.3 19.1 15.8 22.6l57.9 20.9C57.3 229.3 48 259.8 48 291.9v28.1c0 28.4-10.8 57.7-22.3 80.8c-6.5 13-13.9 25.8-22.5 37.6C0 442.7-.9 448.3 .9 453.4s6 8.9 11.2 10.2l64 16c4.2 1.1 8.7 .3 12.4-2s6.3-6.1 7.1-10.4c8.6-42.8 4.3-81.2-2.1-108.7C90.3 344.3 86 329.8 80 316.5V291.9c0-30.2 10.2-58.7 27.9-81.5c12.9-15.5 29.6-28 49.2-35.7l157-61.7c8.2-3.2 17.5 .8 20.7 9s-.8 17.5-9 20.7l-157 61.7c-12.4 4.9-23.3 12.4-32.2 21.6l159.6 57.6c7.6 2.7 15.6 4.1 23.7 4.1s16.1-1.4 23.7-4.1L624.2 182.6c9.5-3.4 15.8-12.5 15.8-22.6s-6.3-19.1-15.8-22.6L343.7 36.1C336.1 33.4 328.1 32 320 32zM128 408c0 35.3 86 72 192 72s192-36.7 192-72L496.7 262.6 354.5 314c-11.1 4-22.8 6-34.5 6s-23.5-2-34.5-6L143.3 262.6 128 408z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Universidad</span
                                            >
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center py-3 px-4 text-gray-900 rounded-lg hover:bg-white/10 dark:hover:bg-gray-700 gap-4 group"
                                    >
                                        <svg
                                            aria-hidden="true"
                                            class="w-6 h-6 transition duration-75 group-hover:text-white"
                                            fill="currentColor"
                                            xmlns="http://www.w3.org/2000/svg"
                                            viewBox="0 0 512 512"
                                        >
                                            <!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                            <path
                                                d="M441 58.9L453.1 71c9.4 9.4 9.4 24.6 0 33.9L424 134.1 377.9 88 407 58.9c9.4-9.4 24.6-9.4 33.9 0zM209.8 256.2L344 121.9 390.1 168 255.8 302.2c-2.9 2.9-6.5 5-10.4 6.1l-58.5 16.7 16.7-58.5c1.1-3.9 3.2-7.5 6.1-10.4zM373.1 25L175.8 222.2c-8.7 8.7-15 19.4-18.3 31.1l-28.6 100c-2.4 8.4-.1 17.4 6.1 23.6s15.2 8.5 23.6 6.1l100-28.6c11.8-3.4 22.5-9.7 31.1-18.3L487 138.9c28.1-28.1 28.1-73.7 0-101.8L474.9 25C446.8-3.1 401.2-3.1 373.1 25zM88 64C39.4 64 0 103.4 0 152V424c0 48.6 39.4 88 88 88H360c48.6 0 88-39.4 88-88V312c0-13.3-10.7-24-24-24s-24 10.7-24 24V424c0 22.1-17.9 40-40 40H88c-22.1 0-40-17.9-40-40V152c0-22.1 17.9-40 40-40H200c13.3 0 24-10.7 24-24s-10.7-24-24-24H88z"
                                            />
                                        </svg>
                                        <div class="group">
                                            <span
                                                class="text-sm font-bold hover:text-white group-hover:text-white"
                                                >Tareas</span
                                            >
                                        </div>
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </Sidebar>
                <Button icon="pi pi-align-left" @click="visible = true" />
            </div>
            <!-- <form @submit.prevent="logout">
                <Button label="Logout" icon="pi pi-sign-out" type="submit" />
            </form> -->

            <Avatar
                label="P"
                class="mr-2 cursor-pointer hover:scale-105"
                size="large"
                shape="circle"
                @click="toggleMenu"
            />

            <div
                class="card flex justify-content-center absolute -bottom-48 right-2"
                v-if="showMenu"
            >
                <Menu :model="items">
                    <template #start>
                        <button
                            @click="profileClick"
                            class="w-full p-link flex gap-3 items-center text-color hover:surface-200 border-noround"
                        >
                            <Avatar
                                image="https://primefaces.org/cdn/primevue/images/avatar/amyelsner.png"
                                class="ml-2"
                                shape="circle"
                            />
                            <div class="flex flex-col">
                                <span class="font-bold">Amy Elsner</span>
                                <span class="text-sm">Agent</span>
                            </div>
                        </button>
                    </template>
                    <template #end>
                        <form @submit.prevent="logout">
                            <button
                                class="w-full flex items-center p-2 pl-7 text-color hover:surface-200 border-noround"
                            >
                                <i class="pi pi-sign-out" />
                                <span class="ml-2">Cerrar Session</span>
                            </button>
                        </form>
                    </template>
                </Menu>
            </div>
            <!-- <Avatar
                :image="avatar"
                class="ml-auto cursor-pointer"
                @click="toggleMenu"
            >
                <template #menu>
                    <ul
                        class="p-2 bg-white shadow-lg rounded"
                        v-show="showMenu"
                        @click="toggleMenu"
                    >
                        <li><a href="#">Profile</a></li>
                        <li><a href="#">Sign out</a></li>
                    </ul>
                </template>
            </Avatar> -->
        </div>
    </div>
</template>

<script>
import { ref } from "vue";

const visible = ref(false);

const items = ref([
    { separator: true },
    { label: "Profile", icon: "pi pi-fw pi-user" },
    { label: "Settings", icon: "pi pi-fw pi-cog" },
    { separator: true },
]);

export default {
    components: {
        Menubar,
        Menu,
        Button,
        Sidebar,
        PanelMenu,
        Avatar,
    },
    data() {
        return {
            showMenu: false,
        };
    },

    methods: {
        // const avatar = ref(
        //     "https://www.primefaces.org/wp-content/uploads/2020/05/placeholder.png"
        // );

        // const showMenu = ref(false);

        toggleMenu() {
            this.showMenu = !this.showMenu;
            console.log("OK");
        },
    },
};
</script>
