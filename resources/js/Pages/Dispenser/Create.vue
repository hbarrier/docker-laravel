<template>
    <MainLayout>
        <main class="w-full flex flex-row h-screen pt-[7vh]">
            <img
                class="w-5/12 object-cover lg:flex hidden"
                src="https://www.picard.fr/on/demandware.static/-/Sites-picard-Library/default/dw6c598d3f/loginSignup/login/login-bg-desktop.jpg"
                alt="illu"
            />
            <section
                class="gap-4 items-center pt-8 lg:w-7/12 w-full mx-auto bg-white pt-20"
            >
                <div class="w-3/4 mx-auto gap-4 flex flex-col">
                    <h1 class="text-[#0311a5] font-semibold text-3xl">
                        Add a Dispenser
                    </h1>
                    <p>Enter a name, location and status to add a dispenser.</p>
                    <form @submit.prevent="create">
                        <div>
                            <div class="flex flex-col gap-4 mt-4">
                                <!-- <label>name</label> -->
                                <input
                                    class="border-2 border-[#a5a5a6] rounded placeholder-[#1d1d21]"
                                    v-model="form.name"
                                    type="text"
                                    placeholder="Dispenser name"
                                />
                                <div v-if="form.errors.name">
                                    {{ form.errors.name }}
                                </div>
                            </div>
                            <div class="flex flex-col gap-4 mt-4">
                                <!-- <label>location</label> -->
                                <input
                                    class="border-2 border-[#a5a5a6] rounded placeholder-[#1d1d21]"
                                    v-model="form.location"
                                    type="text"
                                    placeholder="Dispenser location"
                                />
                            </div>
                            <div class="flex flex-col gap-4 mt-4">
                                <!-- <label for="status-select">status : {{ selected }}</label> -->
                                <select
                                    class="border-2 border-[#a5a5a6] rounded placeholder-[#1d1d21]"
                                    name="status"
                                    v-model="form.status"
                                    id="status-select"
                                >
                                    <option disabled value="">
                                        Choose a status
                                    </option>
                                    <option value="active">active</option>
                                    <option value="inactive">inactive</option>
                                    <option value="pending">pending</option>
                                </select>
                            </div>
                            <div class="flex flex-col gap-4 mt-4">
                                <button
                                    class="bg-[#0311a5] text-white font-semibold rounded py-2 text-lg"
                                    type="submit"
                                >
                                    Create
                                </button>
                            </div>
                        </div>
                    </form>
                </div>
            </section>
        </main>
    </MainLayout>
</template>

<style scoped>
label {
    margin-right: 2em;
}

div {
    padding: 2px;
}
</style>

<script setup>
import { useForm } from "@inertiajs/vue3";
import MainLayout from "../../Layouts/MainLayout.vue";

const form = useForm({
    name: "",
    location: "",
    status: "",
});

const create = () => form.post("/dispenser");
</script>
