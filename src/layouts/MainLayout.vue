<template>
  <q-layout view="lHh Lpr fff">
    <q-header elevated>
      <q-toolbar class="bg-white q-pa-md">
        <q-img src="~assets/logo.png" class="logo" />

        <q-space />

        <q-btn-toggle
          v-model="btnRef"
          color="primary"
          flat
          stretch
          toggle-color="secondary"
          class="gt-sm"
          :options="options"
        />

        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          class="lt-md text-primary"
          @click="toggleLeftDrawer = true"
        />
      </q-toolbar>
    </q-header>

    <q-drawer v-model="toggleLeftDrawer">
      <q-list>
        <q-item v-for="option in options" :key="option.value" clickable>
          <q-item-section>
            {{ option.label }}
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-footer class="bg-accent">
      <q-toolbar :class="[$q.screen.lt.sm ? 'column q-py-lg' : 'row q-pa-xl', 'justify-between']">
        <div>
          <q-img src="~assets/logo-2.png" class="logo" />
          <div class="text-grey-5 q-mt-lg">
            <div>Cavite State University - Imus Campus</div>
            <div>Academic Year 2025-2026</div>
            <div>Bachelor of Science in Computer Science - 4C</div>
          </div>
        </div>

        <div :class="$q.screen.lt.sm ? 'row q-mt-md q-gutter-x-md' : 'row q-gutter-x-xl'">
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
const toggleLeftDrawer = ref(false);
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
