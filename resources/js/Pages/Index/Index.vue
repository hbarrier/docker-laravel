<template>
  <MainLayout>
    <div>
      <h1>{{ message }}</h1>
    </div>
  </MainLayout>
</template>

<script setup>
  import MainLayout from '../../Layouts/MainLayout.vue';

  defineProps({
    message: String
  });
</script>