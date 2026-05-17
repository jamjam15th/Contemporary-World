<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="bg-white">
        <q-img
          src="src/assets/logo.png"
          class="logo"
        />

        <q-space />

        <q-btn-toggle
          v-model="btnRef"
          color="primary"
          flat
          stretch
          toggle-color="secondary"
          :options="options"
        />
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const btnRef = ref('Home');

const options = [
  { label: 'Home', value: 'Home' },
  { label: 'Globalization', value: 'Globalization' },
  { label: 'Areas of Impact', value: 'Areas of Impact' },
  { label: 'Meet the Team', value: 'Meet the Team' },
];
</script>

<style scoped lang="sass">
.logo
  width: clamp(80px, 15vw, 120px)
</style>
