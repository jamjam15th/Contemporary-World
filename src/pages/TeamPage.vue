<template>
  <q-page class="bg-white flex flex-center q-pa-md">
    <div class="full-width" style="max-width: 1000px; margin: 0 auto; padding: 60px 0;">

      <!-- Title -->
      <div class="team-title text-weight-bold text-center q-mb-xl">
        Meet the Team
      </div>

      <!-- 2x2 Grid: Pinalitan natin ang col-md-6 ng col-sm-6 -->
      <div class="row q-col-gutter-y-xl q-col-gutter-x-md justify-center">
        <div
          class="col-12 col-sm-6 flex column items-center"
          v-for="team in teams"
          :key="team.role"
        >
          <!-- Gradient Pill -->
          <div class="role-pill shadow-3 q-mb-md">
            {{ team.role }}
          </div>

          <!-- Members -->
          <div class="text-center text-grey-9 member-text">
            <div v-for="member in team.members" :key="member" class="text-weight-medium">
              {{ member }}
            </div>
          </div>
        </div>
      </div>

    </div>
  </q-page>
</template>

<script setup lang="ts">
const teams = [
  {
    role: 'Developers',
    members: ['Jamil S. Mariano', 'Carl Janielle B. Peralta']
  },
  {
    role: 'UX/UI Designers',
    members: ['Rachelle Yazmhine C. Mendez', 'Borja, Ma. Liel Fatyma B.']
  },
  {
    role: 'Content Researchers',
    members: ['Jobel King Bautista', 'Shiela Mae Ann R. Azul']
  },
  {
    role: 'Content Editors',
    members: ['Rachelle Yazmhine C. Mendez', 'Maricar An Mae Gallego']
  }
];
</script>

<style scoped lang="scss">
@mixin mobile {
  @media (max-width: 599px) {
    @content;
  }
}
@mixin tablet_desktop {
  @media (min-width: 600px) {
    @content;
  }
}

.team-title {
  color: #3b8e96;
  @include mobile {
    font-size: 10vw;
    margin-bottom: 40px;
  }
  @include tablet_desktop {
    font-size: clamp(32px, 15vw, 60px);
    margin-bottom: 60px;
  }
}

.role-pill {
  background: linear-gradient(90deg, #1c5271 0%, #329d9c 100%);
  color: white;
  font-weight: 600;
  border-radius: 50px;
  padding: 12px 30px;
  width: 100%;
  max-width: 280px;
  text-align: center;
  letter-spacing: 0.5px;

  @include mobile {
    font-size: clamp(14px, 3.5vw, 16px);
  }
  @include tablet_desktop {
    font-size: clamp(14px, 1.2vw, 16px);
  }
}

.member-text {
  line-height: 1.6;
  @include mobile {
    font-size: clamp(14px, 3.5vw, 16px);
  }
  @include tablet_desktop {
    font-size: clamp(14px, 5vw, 20px);
  }
}
</style>
