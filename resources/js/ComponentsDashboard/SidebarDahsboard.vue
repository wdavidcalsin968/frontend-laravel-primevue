<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import Welcome from '@/Components/Welcome.vue';
</script>

<template>
    <AppLayout title="Dashboard">
        <div class="card flex justify-content-center">
            <Sidebar v-model:visible="visible">
                <h2>Sidebar</h2>
                <p></p>
            </Sidebar>
            <Button icon="pi pi-arrow-right" @click="visible = true" />
        </div>
    </AppLayout>
</template>

<script setup>
import { ref } from "vue";

const visible = ref(false);
</script>