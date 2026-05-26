<template>
  <q-page>
    <!-- Hero Section -->
    <q-img src="~assets/technology/hero-bg.png" style="background-color: #2c3e50" :ratio="16 / 9">
      <div class="text-center flex flex-center column bg-transparent full-height full-width">
        <div class="hero-title text-weight-bold q-mb-sm text-white">Technology</div>
        <div class="hero-subtitle text-weight-medium text-white">
          <div>The Digital Infrastructure of a Borderless World</div>
        </div>
      </div>
    </q-img>

    <!-- AI & ML Section -->
    <div class="row flex flex-center q-mt-lg q-mt-xl-md q-mb-xl">
      <div
        class="col-12 col-sm-6"
        :class="$q.screen.width > $q.screen.height ? 'text-left q-pa-xl' : ' text-center q-pa-md '"
      >
        <div class="connecting-title">Artificial Intelligence</div>
        <div class="connecting-title text-weight-bold">and Machine Learning</div>
        <div class="connecting-body text-weight-medium q-mt-md">
          Learn that tools, they are reshaping the art, artifact hub with hardware, status quo and agile anew.
        </div>
      </div>
      <div class="col-12 col-sm-6 q-pa-md">
        <q-carousel
          v-model="aiSlide"
          transition-prev="slide-right"
          transition-next="slide-left"
          swipeable
          animated
          control-color="primary"
          navigation
          padding
          arrows
          height="400px"
          class="bg-transparent rounded-borders"
        >
          <q-carousel-slide name="automation" img-src="~assets/technology/ai-ml/ai-automation.png">
            <div class="absolute-top text-center q-mt-md">
              <q-chip color="white" text-color="primary" class="text-weight-bold" size="lg">Automation</q-chip>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="healthcare" img-src="~assets/technology/ai-ml/ai-healthcare.png">
            <div class="absolute-top text-center q-mt-md">
              <q-chip color="white" text-color="primary" class="text-weight-bold" size="lg">Healthcare</q-chip>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="education" img-src="~assets/technology/ai-ml/ai-education.png">
            <div class="absolute-top text-center q-mt-md">
              <q-chip color="white" text-color="primary" class="text-weight-bold" size="lg">Education</q-chip>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="agriculture" img-src="~assets/technology/ai-ml/ai-agriculture.png">
            <div class="absolute-top text-center q-mt-md">
              <q-chip color="white" text-color="primary" class="text-weight-bold" size="lg">Agriculture</q-chip>
            </div>
          </q-carousel-slide>
        </q-carousel>
      </div>
    </div>

    <!-- 5G in Action Banner -->
    <div class="bg-teal-7 text-white q-py-xl q-mt-xl">
      <div class="row justify-center" :class="$q.screen.width > $q.screen.height ? 'q-px-xl' : 'q-px-md'">
        <div class="col-12 col-md-10" :class="$q.screen.width > $q.screen.height ? 'text-left' : 'text-center'">
          <div class="text-italic q-mb-sm" style="font-size: clamp(20px, 3vw, 36px);">5G in Action</div>
          <div class="text-weight-bold q-mb-md" style="font-size: clamp(24px, 4vw, 48px); line-height: 1.2;">
            The Real-World Impacts of a Connected World
          </div>
          <div class="text-weight-regular" style="font-size: clamp(14px, 1.5vw, 20px);">
            In 2023, 5G is the connection tissue transforming how global interaction operates, enabling faster connectivity, era for dynamics to un-tangle new nations, people and lays out a common future.
          </div>
        </div>
      </div>
    </div>

    <!-- Use Cases Grid -->
    <div
      class="row justify-center q-py-xl"
      :class="$q.screen.width > $q.screen.height ? 'q-px-xl' : 'q-px-md'"
    >
      <div class="col-12 col-lg-10">
        <div class="row q-col-gutter-xl">
          
          <!-- Item 1: Nokia -->
          <div class="col-12 col-md-6">
            <div class="q-mb-md">
              <q-img src="~assets/technology/logos/logo-nokia.png" height="50px" fit="contain" position="left" class="q-mb-sm" />
              <div class="text-weight-bold text-grey-10 q-mb-xs" style="font-size: clamp(18px, 1.8vw, 24px);">
                Nokia: Smart agriculture
              </div>
              <div class="text-grey-7 q-mb-md text-weight-medium">
                Climate & Environment
              </div>
              <q-img src="~assets/technology/cards/nokia-agri.png" :ratio="16/9" style="border-radius: 12px; border: 1px solid #eee;" class="q-mb-md" />
              <div class="text-grey-9" style="font-size: clamp(14px, 1.1vw, 16px); line-height: 1.6;">
                By utilizing 5G and IoT sensors, rural farms can monitor crops and machinery telemetry in real-time. This connected approach bridges the digital divide, reduces necessary pesticide use, and increases overall global crop yields.
              </div>
            </div>
          </div>

          <!-- Item 2: Pymetrics -->
          <div class="col-12 col-md-6">
            <div class="q-mb-md">
              <q-img src="~assets/technology/logos/logo-pymetrics.png" height="50px" fit="contain" position="left" class="q-mb-sm" />
              <div class="text-weight-bold text-grey-10 q-mb-xs" style="font-size: clamp(18px, 1.8vw, 24px);">
                Pymetrics: Gamified recruiting tool powered by AI
              </div>
              <div class="text-grey-7 q-mb-md text-weight-medium">
                Global Governance & Human Rights
              </div>
              <q-img src="~assets/technology/cards/pymetrics-ui.png" :ratio="16/9" style="border-radius: 12px; border: 1px solid #eee;" class="q-mb-md" />
              <div class="text-grey-9" style="font-size: clamp(14px, 1.1vw, 16px); line-height: 1.6;">
                This gamified, AI-powered recruiting tool replaces traditional resumes with unbiased, ethical algorithms. Deployed across 68 countries, it has significantly increased hiring diversity across gender, ethnicity, and socio-economic status on a global scale.
              </div>
            </div>
          </div>

          <!-- Item 3: KT -->
          <div class="col-12 col-md-6">
            <div class="q-mb-md">
              <q-img src="~assets/technology/logos/logo-kt.png" height="50px" fit="contain" position="left" class="q-mb-sm" />
              <div class="text-weight-bold text-grey-10 q-mb-xs" style="font-size: clamp(18px, 1.8vw, 24px);">
                Korea Telecom: Skyship: 5G emergency rescue platform
              </div>
              <div class="text-grey-7 q-mb-md text-weight-medium">
                Migration & Crisis Response
              </div>
              <q-img src="~assets/technology/cards/kt-skyship.png" :ratio="16/9" style="border-radius: 12px; border: 1px solid #eee;" class="q-mb-md" />
              <div class="text-grey-9" style="font-size: clamp(14px, 1.1vw, 16px); line-height: 1.6;">
                Skyship is a bespoke 5G airship functioning as a mobile communication center for disaster management. It deploys and remotely controls drones and robots to locate and assist disaster survivors in compromised or hard-to-reach areas.
              </div>
            </div>
          </div>

          <!-- Item 4: Quantela -->
          <div class="col-12 col-md-6">
            <div class="q-mb-md">
              <q-img src="~assets/technology/logos/logo-quantela.png" height="50px" fit="contain" position="left" class="q-mb-sm" />
              <div class="text-weight-bold text-grey-10 q-mb-xs" style="font-size: clamp(18px, 1.8vw, 24px);">
                Quantela: IoT and smart city solutions
              </div>
              <div class="text-grey-7 q-mb-md text-weight-medium">
                Tech & Digital Culture
              </div>
              <q-img src="~assets/technology/cards/quantela-ui.png" :ratio="16/9" style="border-radius: 12px; border: 1px solid #eee;" class="q-mb-md" />
              <div class="text-grey-9" style="font-size: clamp(14px, 1.1vw, 16px); line-height: 1.6;">
                As global populations urbanize, this AI-powered IoT platform provides real-time, predictive analytics to manage city infrastructure. These smart investments optimize energy grids, reduce CO2 emissions, and enhance disaster response capabilities.
              </div>
            </div>
          </div>

          <!-- Item 5: J&J -->
          <div class="col-12 col-md-6">
            <div class="q-mb-md">
              <q-img src="~assets/technology/logos/logo-jnj.png" height="50px" fit="contain" position="left" class="q-mb-sm" />
              <div class="text-weight-bold text-grey-10 q-mb-xs" style="font-size: clamp(18px, 1.8vw, 24px);">
                Johnson & Johnson: VR-based training programme for doctors
              </div>
              <div class="text-grey-7 q-mb-md text-weight-medium">
                Global Education
              </div>
              <q-img src="~assets/technology/cards/jnj-vr.png" :ratio="16/9" style="border-radius: 12px; border: 1px solid #eee;" class="q-mb-md" />
              <div class="text-grey-9" style="font-size: clamp(14px, 1.1vw, 16px); line-height: 1.6;">
                A global virtual reality training program allows surgeons and nurses to simulate real-world operating room experiences. This digital knowledge-sharing provides advanced medical skill enhancement to practitioners around the world without the need for extensive travel.
              </div>
            </div>
          </div>

          <!-- Item 6: Ericsson -->
          <div class="col-12 col-md-6">
            <div class="q-mb-md">
              <q-img src="~assets/technology/logos/logo-ericsson.png" height="50px" fit="contain" position="left" class="q-mb-sm" />
              <div class="text-weight-bold text-grey-10 q-mb-xs" style="font-size: clamp(18px, 1.8vw, 24px);">
                Ericsson: EMH – Remote patient monitoring
              </div>
              <div class="text-grey-7 q-mb-md text-weight-medium">
                Universal Access
              </div>
              <q-img src="~assets/technology/cards/ericsson-emh.png" :ratio="16/9" style="border-radius: 12px; border: 1px solid #eee;" class="q-mb-md" />
              <div class="text-grey-9" style="font-size: clamp(14px, 1.1vw, 16px); line-height: 1.6;">
                The Ericsson Mobile Health platform utilizes mobile networks to monitor patients' physiological parameters in near real-time. This creates a system of decentralized care, helping to ensure that life-saving healthcare access can reach populations anywhere.
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const aiSlide = ref('automation');
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
    font-size: 6vw;
  }
  @include landscape {
    font-size: 5vw;
  }
}

.hero-subtitle {
  @include portrait {
    font-size: 3vw;
  }
  @include landscape {
    font-size: 1.5vw;
  }
}

.connecting-title {
  @include portrait {
    font-size: 5vw;
  }
  @include landscape {
    line-height: 1.15;
    font-size: 3.8vw;
  }
}

.connecting-body {
  @include portrait {
    font-size: clamp(14px, 2.3vw, 18px);
  }
  @include landscape {
    font-size: 1.5vw;
  }
}
</style>
