<template>
    <MainLayout>
        <div class="flex flex-row mb-8 justify-between w-11/12 mx-auto pt-24">
            <h1 class="list-none text-4xl text-[#459bab] font-bold">
                All Dispensers
            </h1>
        </div>
        <section class="grid lg:grid-cols-2 gap-4 items-center w-11/12 mx-auto">
            <div v-for="dispenser in sortedDispensers" :key="dispenser.id">
                <Link :href="`/dispenser/${dispenser.id}`">
                    <DispenserInfos :dispenser="dispenser" />
                </Link>
            </div>
        </section>
    </MainLayout>
</template>

<script setup>
import { computed } from "vue";
import { Link } from "@inertiajs/vue3";
import DispenserInfos from "@/Components/DispenserInfos.vue";
import MainLayout from "../../Layouts/MainLayout.vue";

const props = defineProps({
    dispensers: Array,
});

const sortedDispensers = computed(() => {
    return props.dispensers
        .slice()
        .sort((a, b) => new Date(b.created_at) - new Date(a.created_at));
});
</script>
