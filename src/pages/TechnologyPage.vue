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
    <div style="max-width: 1200px; margin: 0 auto;">
      <div class="row flex flex-center q-mt-lg q-mt-xl-md q-mb-xl">
      <div
        class="col-12 col-sm-6"
        :class="$q.screen.width > $q.screen.height ? 'text-left q-pr-xl q-py-xl' : 'text-center q-pa-md'"
      >
        <div class="text-weight-bold" style="font-size: clamp(32px, 3.5vw, 46px); line-height: 1.1; letter-spacing: -0.5px;">Artificial Intelligence</div>
        <div class="text-weight-bold" style="font-size: clamp(32px, 3.5vw, 46px); line-height: 1.1; letter-spacing: -0.5px;">and Machine Learning</div>
        <div class="text-weight-medium q-mt-lg" style="color: #4f4f4f; font-size: clamp(16px, 1.2vw, 18px); line-height: 1.6; padding-right: 20px;">
          aren't just tools, they are reshaping the entire fields such as healthcare, education, and agriculture.
        </div>
      </div>
      <div class="col-12 col-sm-6 q-pa-md">
        <q-carousel
          v-model="aiSlide"
          transition-prev="slide-right"
          transition-next="slide-left"
          swipeable
          animated
          control-color="dark"
          :navigation="false"
          height="auto"
          class="bg-transparent"
        >

          <q-carousel-slide name="automation" class="q-pa-none">
            <div class="relative-position">
              <q-img src="~assets/technology/ai-ml/ai-automation.png" :ratio="16/9" style="border-radius: 12px;" />
              <div class="absolute-top-right q-pa-sm">
                <div class="bg-white text-dark text-weight-bold shadow-1" style="border-radius: 20px; font-size: 13px; padding: 6px 16px; margin: 8px;">
                  Automation
                </div>
              </div>
            </div>
          </q-carousel-slide>
          
          <q-carousel-slide name="healthcare" class="q-pa-none">
            <div class="relative-position">
              <q-img src="~assets/technology/ai-ml/ai-healthcare.png" :ratio="16/9" style="border-radius: 12px;" />
              <div class="absolute-top-right q-pa-sm">
                <div class="bg-white text-dark text-weight-bold shadow-1" style="border-radius: 20px; font-size: 13px; padding: 6px 16px; margin: 8px;">
                  Healthcare
                </div>
              </div>
            </div>
          </q-carousel-slide>

          <q-carousel-slide name="education" class="q-pa-none">
            <div class="relative-position">
              <q-img src="~assets/technology/ai-ml/ai-education.png" :ratio="16/9" style="border-radius: 12px;" />
              <div class="absolute-top-right q-pa-sm">
                <div class="bg-white text-dark text-weight-bold shadow-1" style="border-radius: 20px; font-size: 13px; padding: 6px 16px; margin: 8px;">
                  Education
                </div>
              </div>
            </div>
          </q-carousel-slide>

          <q-carousel-slide name="agriculture" class="q-pa-none">
            <div class="relative-position">
              <q-img src="~assets/technology/ai-ml/ai-agriculture.png" :ratio="16/9" style="border-radius: 12px;" />
              <div class="absolute-top-right q-pa-sm">
                <div class="bg-white text-dark text-weight-bold shadow-1" style="border-radius: 20px; font-size: 13px; padding: 6px 16px; margin: 8px;">
                  Agriculture
                </div>
              </div>
            </div>
          </q-carousel-slide>
        </q-carousel>
        <div class="row justify-center q-mt-lg q-gutter-md">
          <div class="cursor-pointer" style="width: 10px; height: 10px; border-radius: 50%;" :style="aiSlide === 'automation' ? 'background-color: #1a1a1a;' : 'border: 2px solid #1a1a1a;'" @click="aiSlide = 'automation'"></div>
          <div class="cursor-pointer" style="width: 10px; height: 10px; border-radius: 50%;" :style="aiSlide === 'healthcare' ? 'background-color: #1a1a1a;' : 'border: 2px solid #1a1a1a;'" @click="aiSlide = 'healthcare'"></div>
          <div class="cursor-pointer" style="width: 10px; height: 10px; border-radius: 50%;" :style="aiSlide === 'education' ? 'background-color: #1a1a1a;' : 'border: 2px solid #1a1a1a;'" @click="aiSlide = 'education'"></div>
          <div class="cursor-pointer" style="width: 10px; height: 10px; border-radius: 50%;" :style="aiSlide === 'agriculture' ? 'background-color: #1a1a1a;' : 'border: 2px solid #1a1a1a;'" @click="aiSlide = 'agriculture'"></div>
        </div>
      </div>
    </div>
    </div>

    <!-- 5G in Action Banner -->
    <div class="text-white q-py-xl q-mt-xl" style="background: linear-gradient(90deg, #205072 0%, #329D9C 100%);">
      <div
        :class="$q.screen.width > $q.screen.height ? 'q-px-xl' : 'q-px-md'"
        style="max-width: 1200px; margin: 0 auto;"
      >
        <div :class="$q.screen.width > $q.screen.height ? 'text-left' : 'text-center'">
          <div class="text-italic text-weight-bold q-mb-sm" style="font-size: clamp(32px, 5vw, 48px); letter-spacing: 1px;">5G in Action</div>
          <div class="text-weight-bold q-mb-md" style="font-size: clamp(28px, 4.5vw, 42px); line-height: 1.2; letter-spacing: 0.5px;">
            The Real-World Impacts of a Connected World
          </div>
          <div class="text-weight-regular" style="font-size: clamp(16px, 1.5vw, 18px); line-height: 1.6; max-width: 1000px; letter-spacing: 0.3px; word-spacing: 1px;">
            In 2025, <b>5G</b> is the connective tissue transforming how global industries operate, enabling faster connectivity and fundamentally changing how nations, people, and systems communicate.
          </div>
        </div>
      </div>
    </div>

    <!-- Use Cases Grid -->
    <div>
      <div
        class="q-py-xl"
        :class="$q.screen.width > $q.screen.height ? 'q-px-xl' : 'q-px-md'"
        style="max-width: 1200px; margin: 0 auto;"
      >
        <!-- Row 1: Nokia + Pymetrics -->
        <div class="row q-col-gutter-xl q-pb-xl">
          <!-- Nokia -->
          <div class="col-12 col-md-6">
            <div class="use-case-card card-left-col">
              <img src="~assets/technology/logos/logo-nokia.png" class="use-case-logo" alt="Nokia" />
              <div class="use-case-subtitle">Smart agriculture</div>
              <q-img src="~assets/technology/cards/nokia-agri.png" class="use-case-img q-mb-sm" />
              <div class="use-case-desc">
                By utilizing 5G and IoT sensors, rural farms can monitor crops and machinery telemetry in real-time. This connected approach bridges the digital divide, reduces necessary pesticide use, and increases overall global crop yields.
              </div>
            </div>
          </div>
          <!-- Pymetrics -->
          <div class="col-12 col-md-6">
            <div class="use-case-card card-right-col">
              <img src="~assets/technology/logos/logo-pymetrics.png" class="use-case-logo" alt="Pymetrics" />
              <div class="use-case-subtitle">Gamified recruiting tool powered by AI</div>
              <q-img src="~assets/technology/cards/pymetrics-ui.png" class="use-case-img q-mb-sm" />
              <div class="use-case-desc">
                This gamified, AI-powered recruiting tool replaces traditional resumes with unbiased, ethical algorithms. Deployed across 68 countries, it has significantly increased hiring diversity across gender, ethnicity, and socio-economic status on a global scale.
              </div>
            </div>
          </div>
        </div>

        <!-- Row 2: KT + Quantela -->
        <div class="row q-col-gutter-xl q-pb-xl">
          <!-- KT -->
          <div class="col-12 col-md-6">
            <div class="use-case-card card-left-col">
              <img src="~assets/technology/logos/logo-kt.png" class="use-case-logo" alt="Korea Telecom" />
              <div class="use-case-subtitle">Skyship: 5G emergency rescue platform</div>
              <q-img src="~assets/technology/cards/kt-skyship.png" class="use-case-img q-mb-sm" />
              <div class="use-case-desc">
                Skyship is a bespoke 5G airship functioning as a mobile communication center for disaster management. It deploys and remotely controls drones and robots to locate and assist disaster survivors in compromised or hard-to-reach areas.
              </div>
            </div>
          </div>
          <!-- Quantela -->
          <div class="col-12 col-md-6">
            <div class="use-case-card card-right-col">
              <img src="~assets/technology/logos/logo-quantela.png" class="use-case-logo" alt="Quantela" />
              <div class="use-case-subtitle">IoT and smart city solutions</div>
              <q-img src="~assets/technology/cards/quantela-ui.png" class="use-case-img q-mb-sm" />
              <div class="use-case-desc">
                As global populations urbanize, this AI-powered IoT platform provides real-time, predictive analytics to manage city infrastructure. These smart investments optimize energy grids, reduce CO2 emissions, and enhance disaster response capabilities.
              </div>
            </div>
          </div>
        </div>

        <!-- Row 3: J&J + Ericsson -->
        <div class="row q-col-gutter-xl q-pb-xl">
          <!-- J&J -->
          <div class="col-12 col-md-6">
            <div class="use-case-card card-left-col">
              <img src="~assets/technology/logos/logo-jnj.png" class="use-case-logo" alt="Johnson and Johnson" />
              <div class="use-case-subtitle">VR-based training programme for doctors</div>
              <q-img src="~assets/technology/cards/jnj-vr.png" :ratio="16/9" class="use-case-img q-mb-sm" />
              <div class="use-case-desc">
                A global virtual reality training program allows surgeons and nurses to simulate real-world operating room experiences. This digital knowledge-sharing provides advanced medical skill enhancement to practitioners around the world without the need for extensive travel.
              </div>
            </div>
          </div>
          <!-- Ericsson -->
          <div class="col-12 col-md-6">
            <div class="use-case-card card-right-col">
              <img src="~assets/technology/logos/logo-ericsson.png" class="use-case-logo" alt="Ericsson" />
              <div class="use-case-subtitle">EMH – Remote patient monitoring</div>
              <q-img src="~assets/technology/cards/ericsson-emh.png" :ratio="16/9" class="use-case-img q-mb-sm" />
              <div class="use-case-desc">
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

.use-case-card {
  text-align: left;
}

.use-case-logo {
  display: block;
  height: 32px;
  max-width: 100%;
  width: auto;
  object-fit: contain;
  object-position: left bottom;
  margin-bottom: 12px;
}

.card-left-col {
  padding-right: clamp(0px, 2vw, 40px);
}

.card-right-col {
  padding-left: clamp(0px, 2vw, 40px);
}

.use-case-subtitle {
  font-size: clamp(15px, 1.5vw, 19px);
  font-weight: 700;
  color: #1a1a1a;
  margin-bottom: 12px;
}

.use-case-img {
  width: 100%;
  border-radius: 0;
}

.use-case-desc {
  font-size: clamp(12px, 1vw, 14px);
  line-height: 1.55;
  color: #555;
}
</style>
