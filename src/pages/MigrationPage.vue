<template>
  <q-page>
    <!-- Hero Section -->
    <q-img src="~assets/Migration/human-cost.png" style="background-color: #2c3e50" :ratio="16 / 9">
      <div class="text-center flex flex-center column full-height full-width" style="background: rgba(0, 0, 0, 0.6);">
        <q-chip
          class="bg-white text-dark text-weight-bold q-mb-md"
        >
          Migration and Displacement
        </q-chip>
        <div class="hero-title text-weight-bold q-mb-sm text-white">
          The Human Cost of a Changing World
        </div>
        <div class="hero-subtitle text-weight-medium text-white q-mt-sm">
          By mid-2025, 117.3 million people had been forcibly displaced by persecution, conflict, violence, and
          human rights violations. As global temperatures shift and conflicts arise, displacement is no longer
          just a local issue. It is a defining characteristic of our modern, interconnected era.
        </div>
      </div>
    </q-img>

    <!-- Content Sections -->
    <div style="max-width: 1200px; margin: 0 auto; padding-top: 40px; padding-bottom: 40px;">
      
      <!-- The Past Decade -->
      <div class="row items-center q-mb-xl q-mt-md">
        <div class="col-12 col-md-6 q-pa-md">
          <q-img src="~assets/Migration/past-decade.png" style="border-radius: 8px;" />
        </div>
        <div class="col-12 col-md-6 q-pa-md">
          <div :class="$q.screen.width > $q.screen.height ? 'text-left q-pl-xl' : 'text-center'">
            <div class="text-weight-bold text-dark q-mb-md section-title">
              The Past Decade
            </div>
            <div class="text-weight-regular section-body">
              Weather-related disasters caused roughly 250 million internal displacements, equating to 70,000 people uprooted every single day.
            </div>
          </div>
        </div>
      </div>

      <!-- The Present Reality -->
      <div class="row items-center q-mb-xl">
        <div class="col-12 col-md-6 q-pa-md" :style="$q.screen.width <= $q.screen.height ? 'order: 2' : 'order: 1'">
          <div :class="$q.screen.width > $q.screen.height ? 'text-left q-pr-xl' : 'text-center'">
            <div class="text-weight-bold text-dark q-mb-md section-title">
              The Present Reality
            </div>
            <div class="text-weight-regular section-body">
              Displacement and environmental risk have collided. Today, three out of four forcibly displaced individuals are living in regions with extreme exposure to climate hazards.
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 q-pa-md" :style="$q.screen.width <= $q.screen.height ? 'order: 1' : 'order: 2'">
          <q-img src="~assets/Migration/present-reality.png" style="border-radius: 8px;" />
        </div>
      </div>

      <!-- The 2050 Projection -->
      <div class="row items-center q-mb-xl">
        <div class="col-12 col-md-6 q-pa-md">
          <q-img src="~assets/Migration/2050-projection.png" style="border-radius: 8px;" />
        </div>
        <div class="col-12 col-md-6 q-pa-md">
          <div :class="$q.screen.width > $q.screen.height ? 'text-left q-pl-xl' : 'text-center'">
            <div class="text-weight-bold text-dark q-mb-md section-title">
              The 2050 Projection
            </div>
            <div class="text-weight-regular section-body">
              With climate migration already in the tens of millions, projections point to a staggering 1.2 billion people potentially displaced by climate change by 2050.
            </div>
          </div>
        </div>
      </div>
      
    </div>

    <!-- The Legal Protection Gap -->
    <div class="q-py-xl" style="padding-bottom: 120px;">
      <div class="text-center" :class="$q.screen.width > $q.screen.height ? 'q-px-xl' : 'q-px-md'" style="max-width: 900px; margin: 0 auto; padding-top: 20px; padding-bottom: 20px;">
        <div class="text-weight-bold q-mb-md" style="color: #329D9C; font-size: clamp(28px, 3.5vw, 42px); line-height: 1.2; letter-spacing: -0.5px;">
          The Legal Protection Gap
        </div>
        <div class="text-weight-regular" style="color: #4f4f4f; font-size: clamp(16px, 1.2vw, 18px); line-height: 1.6;">
          Despite the growing crisis, international law hasn't caught up. Climate migrants have no legally binding protections or agreements that obligate countries to take them in. Unlike officially recognized refugees who fall under the 1951 UN Refugee Convention, climate migrants are largely on their own, leaving millions vulnerable and without formal support.
        </div>
      </div>
    </div>

  </q-page>
</template>

<script setup lang="ts">
// Component logic (if any) can be added here
</script>

<style lang="scss">
@mixin portrait {
  @media (orientation: portrait) {
    @content;
  }
}
@mixin landscape {
  @media (orientation: landscape) {
    @content;
  }
}

.hero-title {
  @include portrait {
    font-size: 4vw;
  }
  @include landscape {
    font-size: 4.5vw;
  }
}

.hero-subtitle {
  max-width: 1000px;
  line-height: 1.6;
  @include portrait {
    font-size: 3vw;
    padding: 0 20px;
  }
  @include landscape {
    font-size: 1.25vw;
    padding: 0;
  }
}

.section-title {
  font-size: clamp(28px, 3.5vw, 42px); 
  line-height: 1.2; 
  letter-spacing: -0.5px;
}

.section-body {
  color: #4f4f4f; 
  font-size: clamp(16px, 1.2vw, 18px); 
  line-height: 1.6;
}
</style>
