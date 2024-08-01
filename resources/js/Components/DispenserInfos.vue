<template>
  <div class="shadow-[0px_0px_20px_0px_rgba(229,231,235,0.3)] rounded-lg transition-all duration-500 bg-white p-6 flex flex-col justify-between w-full lg:h-[17vh] h-[20vh] hover:shadow-[0px_0px_20px_0px_rgba(229,231,235,0.5)]" :class="{'border-gray-200  border duration-100' : active }">
    <div class="flex flex-row justify-between items-center">
      <p class="font-semibold">{{ dispenser.name }}</p>
      <button class="text-[#0311a5] border-[1.5px] rounded-md px-5 py-1 uppercase font-semibold border-[#0311a5]">{{ dispenser.status }}</button>
    </div>
      <p class="flex flex-row gap-4 items-center"><img class="w-4 h-fit" src="https://www.iconpacks.net/icons/2/free-location-icon-2952-thumb.png" alt="location">{{ dispenser.location }}</p>
  </div>
</template>   

<script setup>
  defineProps({
    dispenser: Object,
  });
</script>