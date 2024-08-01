<template>
    <div class="min-h-screen bg-[#f9f9f7] pb-8 w-full">
        <nav
            class="flex flex-row justify-between lg:px-12 px-8 py-4 border-b-[1.5px] border-gray-200 bg-white w-full top-0 fixed"
        >
            <div class="menu flex flex-row gap-2 items-center">
                <img
                    class="w-10 mr-8 h-fit"
                    src="https://upload.wikimedia.org/wikipedia/fr/thumb/e/e1/Logo_Picard_surgel%C3%A9s.png/1260px-Logo_Picard_surgel%C3%A9s.png?20170717143342"
                    alt="logo picard"
                />
                <Link class="text-[#0311a3] font-semibold" href="/dispenser"
                    >Home Page</Link
                >&nbsp;
                <Link
                    class="text-[#0311a3] font-semibold"
                    href="/dispenser/create"
                    >Create Page</Link
                >
            </div>
        </nav>
        <!-- <div v-if="flashSuccess" class="success">
      {{ flashSuccess }}
    </div> -->

        <slot></slot>
    </div>
</template>

<script setup>
import { computed } from "vue";
import { Link, usePage } from "@inertiajs/vue3";

const page = usePage();
const flashSuccess = computed(() => page.props.value.flash.success);
</script>

<style>
.success {
    background-color: green;
    color: white;
}
</style>
