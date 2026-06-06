<template>
  <q-layout view="lHh Lpr fff">
    <q-header elevated>
      <q-toolbar class="bg-white q-pa-md">
        <q-img src="~assets/logo.png" class="logo" />

        <q-space />

        <div class="row gt-sm q-gutter-md">
          <div v-for="(option, index) in navOptions" :key="option.value" class="relative-position">
            <q-btn
              :label="option.label"
              color="primary"
              flat
              @click="
                option.submenu
                  ? (showMenuIndex = showMenuIndex === index ? -1 : index)
                  : navigateTo(option.value)
              "
            />
            <q-menu
              v-if="option.submenu"
              :offset="[0, 8]"
              :model-value="showMenuIndex === index"
              no-parent-event
              @hide="showMenuIndex = -1"
            >
              <q-list>
                <q-item
                  v-for="item in option.submenu"
                  :key="item.value"
                  clickable
                  @click="
                    navigateTo(item.value);
                    showMenuIndex = -1;
                  "
                >
                  <q-item-section>{{ item.label }}</q-item-section>
                </q-item>
              </q-list>
            </q-menu>
          </div>
        </div>

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
        <template v-for="option in navOptions" :key="option.value">
          <q-item-label v-if="option.submenu" header>{{ option.label }}</q-item-label>
          <q-item v-if="!option.submenu" clickable @click="navigateTo(option.value)">
            <q-item-section>{{ option.label }}</q-item-section>
          </q-item>
          <q-item
            v-for="item in option.submenu"
            :key="item.value"
            clickable
            class="q-pl-lg"
            @click="
              navigateTo(item.value);
              toggleLeftDrawer = false;
            "
          >
            <q-item-section>{{ item.label }}</q-item-section>
          </q-item>
        </template>
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
            <div class="cursor-pointer text-grey-4" @click="navigateTo('#overview')">
              Overview
            </div>
            <div class="cursor-pointer text-grey-4" @click="navigateTo('#effects')">
              Its Effects
            </div>
          </div>
          <div class="q-gutter-sm text-grey-5">
            <div class="text-white">Areas of Impact</div>
            <div class="cursor-pointer text-grey-4" @click="navigateTo('technology')">
              Technology
            </div>
            <div class="cursor-pointer text-grey-4" @click="navigateTo('environment')">
              Environment
            </div>
            <div class="cursor-pointer text-grey-4" @click="navigateTo('migration')">
              Migration
            </div>
            <div class="cursor-pointer text-grey-4" @click="navigateTo('rights')">
              Governance
            </div>
            <div class="cursor-pointer text-grey-4" @click="navigateTo('social')">
              Social Media
            </div>
          </div>
          <div class="text-white cursor-pointer" @click="navigateTo('team')">
            Meet the Team
          </div>
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
import { useRouter } from 'vue-router';

const router = useRouter();
const toggleLeftDrawer = ref(false);
const showMenuIndex = ref(-1);

const navOptions = [
  { label: 'Home', value: '' },
  {
    label: 'Globalization',
    value: 'globalization',
    submenu: [
      { label: 'Overview', value: '#overview' },
      { label: 'Its Effects', value: '#effects' },
    ],
  },
  {
    label: 'Areas of Impact',
    value: 'areas-of-impact',
    submenu: [
      { label: 'Technology in Contemporary World', value: 'technology' },
      { label: 'Climate and Environment', value: 'environment' },
      { label: 'Migration and Displacement', value: 'migration' },
      { label: 'Human Rights and Global Governance', value: 'rights' },
      { label: 'Social Media and Digital Culture', value: 'social' },
    ],
  },
  { label: 'References', value: 'references' },
  { label: 'Meet the Team', value: 'team' },
];

const navigateTo = (path: string) => {
  // Handle hash-based navigation (for sections on same page)
  if (path.startsWith('#')) {
    // First navigate to home if not already there
    void router
      .push('/')
      .then(() => {
        // Wait for the component to render, then scroll
        setTimeout(() => {
          const element = document.querySelector(path);
          if (element) {
            element.scrollIntoView({ behavior: 'smooth' });
          }
        }, 100);
      })
      .catch(() => {
        // Handle navigation error silently
      });
    return;
  }

  if (toggleLeftDrawer.value) {
    toggleLeftDrawer.value = false;
  }

  // Reset menu after navigation
  showMenuIndex.value = -1;

  void router.push(`/${path}`).catch(() => {
    // Handle navigation error silently
  });
};
</script>

<style scoped lang="scss">
.logo {
  width: clamp(80px, 15vw, 120px);
}

.cursor-pointer {
  cursor: pointer;
  transition: color 0.2s ease;
}

.cursor-pointer:hover {
  font-weight: 700;
}

</style>
