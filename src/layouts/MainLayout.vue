<template>
  <q-layout view="lHh Lpr fff">
    <q-header elevated>
      <q-toolbar class="bg-white q-pa-lg">
        <q-img src="~assets/logo.png" class="logo" />

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

    <q-footer class="bg-accent">
      <q-toolbar class="q-pa-xl row justify-between">
        <div>
          <q-img src="~assets/logo-2.png" class="logo" />
          <div class="text-grey-5 q-mt-lg">
            <div>Cavite State University - Imus Campus</div>
            <div>Academic Year 2025-2026</div>
            <div>Bachelor of Science in Computer Science - 4C</div>
          </div>
        </div>

        <div class="row q-gutter-x-xl">
          <div class="q-gutter-sm text-grey-5">
            <div class="text-white">Globalization</div>
            <div>Overview</div>
            <div>Its Effects</div>
          </div>
          <div class="q-gutter-sm text-grey-5">
            <div class="text-white">Areas of Impact</div>
            <div>Technology</div>
            <div>Environment</div>
            <div>Migration</div>
            <div>Governance</div>
          </div>
          <div>Meet the Team</div>
        </div>
      </q-toolbar>
    </q-footer>

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

<style scoped lang="scss">
.logo {
  width: clamp(80px, 15vw, 120px);
}
</style>
