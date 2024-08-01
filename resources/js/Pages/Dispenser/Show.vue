<template>
    <MainLayout>
        <div class="flex flex-row mb-8 justify-between w-11/12 mx-auto pt-24">
            <h1 class="list-none text-4xl text-[#459bab] font-bold">
                Dispenser Details
            </h1>
        </div>
        <section class="grid lg:grid-cols-2 gap-4 items-center w-11/12 mx-auto">
            <DispenserInfos :dispenser="dispenser" />
        </section>
    </MainLayout>
</template>

<script setup>
import DispenserInfos from "@/Components/DispenserInfos.vue";
import MainLayout from "../../Layouts/MainLayout.vue";

defineProps({
    dispenser: Object,
});
</script>
