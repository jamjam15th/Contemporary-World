<template>
  <q-page class="bg-white">
    <!-- Hero Section -->
    <q-img src="~assets/rights/bg.png" :ratio="16 / 9">
      <div
        class="full-width full-height flex flex-center column text-center text-white"
        style="background-color: rgba(0, 0, 0, 0.5)"
        :class="$q.screen.gt.xs ? 'q-pa-xl' : 'q-pa-md'"
      >
        <div
          class="bg-white text-primary text-weight-bold q-px-lg q-py-xs tag-title q-mb-md"
          style="border-radius: 50px"
        >
          Human Rights and Global Governance
        </div>
        <div class="hero-title text-weight-bold q-mb-md">The Balance of Power and Protection</div>
        <div class="hero-subtitle">
          In a deeply interconnected world, protecting human rights requires constant negotiation.
          Global governance relies on the delicate balance between international cooperation,
          democratic accountability, and the ever-shifting priorities of sovereign nations.
        </div>
      </div>
    </q-img>

    <!-- Main Container -->
    <div class="main-container" :class="$q.screen.gt.xs ? 'q-px-xl' : 'q-px-md'">
      <!-- Section 1 -->
      <!-- col-12 sa phone (stack), col-sm-6 sa tablet at desktop (side-by-side) -->
      <div class="row q-col-gutter-xl items-center q-py-xl">
        <div class="col-12 col-sm-6">
          <q-img src="~assets/rights/pic1.png" :ratio="16 / 9" class="rounded-borders shadow-2" />
        </div>
        <div class="col-12 col-sm-6">
          <div class="section-title text-weight-bold text-grey-10 q-mb-md">
            The Sovereignty Tension
          </div>
          <div class="section-body text-grey-9 q-mb-md">
            Nations and international bodies often act based on their own political, economic, and
            security priorities.
          </div>
          <div class="section-body text-grey-9">
            According to the United Nations, this leads to a complex balance of cooperation and
            conflict. While countries may support global agreements on paper, they frequently resist
            actions that threaten their sovereignty. This tension often results in unequal
            protections across regions, particularly for minority groups who face limited rights due
            to cultural norms, political control, or national security concerns.
          </div>
        </div>
      </div>

      <!-- Section 2 -->
      <div class="row q-col-gutter-xl items-center q-py-xl">
        <div class="col-12 col-sm-6" :style="$q.screen.gt.xs ? '' : 'order: 2'">
          <div class="section-title text-weight-bold text-grey-10 q-mb-md">
            The Democratic Framework
          </div>  
          <div class="section-body text-grey-9 q-mb-md">
            Democracy is the mechanism that ensures human rights are actually realized. Systems such
            as free elections, the rule of law, and freedom of expression empower citizens to voice
            concerns and demand accountability.
          </div>
          <div class="section-body text-grey-9">
            On a global scale, the United Nations serves as the crucial platform for this process.
            It provides a space where countries can discuss issues, forge agreements, and utilize
            collective action—through treaties, resolutions, and peacekeeping efforts—to protect
            fundamental rights worldwide.
          </div>
        </div>
        <div class="col-12 col-sm-6" :style="$q.screen.gt.xs ? '' : 'order: 1'">
          <q-img src="~assets/rights/pic2.png" :ratio="16 / 9" class="rounded-borders shadow-2" />
        </div>
      </div>
      
      <!-- Adapting to Tomorrow -->
      <div class="flex flex-center q-py-xl q-mb-xl">
        <div class="text-center bottom-content">
          <div class="section-title text-weight-bold teal-title q-mb-lg">Adapting to Tomorrow</div>
          <div class="section-body text-grey-9 q-mb-md">
            Long-term protection of human rights depends on empowerment from the ground up.
            Individuals and communities must be equipped with education, legal awareness, and access
            to resources to advocate for themselves.
          </div>
          <div class="section-body text-grey-9">
            Furthermore, the United Nations emphasizes that human rights frameworks cannot remain
            static. To remain effective, these protections must continuously adapt to modern,
            borderless challenges, including technological advancements, climate change, and global
            migration.
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup lang="ts"></script>

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

.main-container {
  max-width: 1200px;
  margin: 0 auto;
}

.tag-title {
  @include mobile {
    font-size: clamp(10px, 1vw, 14px);
    padding: 6px 16px !important;
    margin-bottom: 12px;
  }
  @include tablet_desktop {
    font-size: clamp(12px, 1vw, 16px);
    letter-spacing: 0.5px;
  }
}

.hero-title {
  @include mobile {
    font-size: clamp(15px, 4vw, 32px);
    line-height: 1.2;
    padding: 0 10px;
  }
  @include tablet_desktop {
    font-size: clamp(32px, 3.5vw, 64px);
    line-height: 1.1;
  }
}

.hero-subtitle {
  line-height: 1.6;
  opacity: 0.95;
  @include mobile {
    font-size: clamp(10px, 2vw, 16px);
    max-width: 90%;
    margin: 0 auto;
  }
  @include tablet_desktop {
    font-size: clamp(14px, 1.3vw, 20px);
    max-width: 65vw;
  }
}

.section-title {
  line-height: 1.2;
  @include mobile {
    font-size: 6.5vw;
  }
  @include tablet_desktop {
    font-size: 2.5vw;
  }
}

.section-body {
  line-height: 1.6;
  @include mobile {
    font-size: clamp(14px, 3.5vw, 18px);
  }
  @include tablet_desktop {
    font-size: 1.2vw;
  }
}

.bottom-content {
  @include mobile {
    max-width: 100%;
  }
  @include tablet_desktop {
    max-width: 60vw;
  }
}

.teal-title {
  color: #3b8e96;
}

.rounded-borders {
  @include mobile {
    border-radius: 8px;
  }
  @include tablet_desktop {
    border-radius: 0.5vw;
  }
}
</style>
