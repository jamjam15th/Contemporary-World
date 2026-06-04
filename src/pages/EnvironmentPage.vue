<template>
  <q-page>
    <q-img src="~assets/environment/bg.png" :ratio="16 / 9">
      <div
        class="bg-transparent full-width full-height flex flex-center column text-center"
        :class="$q.screen.gt.xs ? 'q-pa-xl' : 'q-pa-md'"
      >
        <div
          class="bg-white text-primary text-weight-medium q-px-md q-py-sm tag-title"
          style="border-radius: 20px"
        >
          Climate and Environment
        </div>
        <div class="hero-title text-weight-bold">The Global Climate Challenge</div>
        <div class="hero-subtitle">
          Climate change is the defining challenge of our interconnected world. Threatening global
          <br v-if="$q.screen.gt.xs" />
          food production through shifting weather patterns and raising the risk of catastrophic
          <br v-if="$q.screen.gt.xs" />
          flooding. The scale is global and the consequences are already here.
        </div>
      </div>
    </q-img>

    <div
      class="flex flex-center container-2 text-center"
      :class="$q.screen.gt.xs ? 'q-pa-xl' : 'q-pa-md q-py-xl'"
    >
      <div>
        <div class="section-title q-mb-lg text-weight-bold gradient-text">
          The Globalization Paradox
        </div>
        <div class="section-body">
          Globalization is often seen as an enemy in the conflict against climate change. Climate
          activists sail to <br v-if="$q.screen.gt.xs" />
          international conferences to condemn airlines and shipping companies for their polluting
          ways and call on <br v-if="$q.screen.gt.xs" />
          consumers to limit their “food miles”, the distance that dinner traveled from farm to
          plate.
        </div>
      </div>
    </div>

    <div
      class="effects-section text-white flex flex-center"
      :class="$q.screen.gt.xs ? 'q-py-xl q-px-md' : 'q-py-xl q-px-sm'"
    >
      <div class="row justify-around effects-container-inner" :class="$q.screen.gt.xs ? 'q-col-gutter-lg ' : ''" style="width: 100%; max-width: 1200px;">
        <div
          class="col-12 col-sm-4 text-center flex-center column q-pa-lg"
          v-for="effect in effects"
          :key="effect.title"
        >
          <q-img :src="effect.image" class="effect-image q-mb-lg" fit="contain" />
          <div class="effect-title text-weight-bold q-mb-md" v-html="effect.title"></div>
          <div class="effect-body text-white">
            {{ effect.body }}
          </div>
        </div>
      </div>
    </div>

    <div
      class="flex flex-center container-2 text-center"
      :class="$q.screen.gt.xs ? 'q-pa-xl' : 'q-pa-md q-py-xl'"
    >
      <div>
        <div class="section-title q-mb-lg text-weight-bold gradient-text">
          Decoupling Growth from Emissions
        </div>
        <div class="section-body">
          Globalization has been a huge force for worldwide prosperity, and historically, prosperity
          has meant more <br v-if="$q.screen.gt.xs" />
          greenhouse gas emissions. But the only practical response to greenhouse gas emissions is
          to decouple <br v-if="$q.screen.gt.xs" />
          economic growth from emissions.
        </div>
      </div>
    </div>

    <q-img src="~assets/environment/bg-2.png" :ratio="16 / 9">
      <div
        class="bg-transparent full-width full-height flex column justify-start text-white"
        :class="$q.screen.gt.xs ? 'q-pa-xl' : 'q-pa-md flex-center text-center'"
      >
        <div
          :class="$q.screen.gt.xs ? 'q-ml-xl q-mt-xl' : ''"
          style="max-width: 700px"
        >
          <div class="roi-title text-weight-bold q-mb-md">The ROI of Climate Resilience</div>
          <div class="roi-body text-weight-regular" style="line-height: 1.5">
            Adapting to climate change isn't just an environmental necessity; it is an economic
            imperative. Research indicates that every $1 invested in climate resilience can return
            more than $10.50 in economic, social, and environmental benefits over the next ten
            years.
          </div>
        </div>
      </div>
    </q-img>

    <div
      class="explore-container"
      :class="$q.screen.gt.xs ? 'q-py-xl' : 'q-py-lg'"
    >
      <div class="explore-title text-center text-weight-bold text-grey-9">Explore the Data:</div>

      <div
        class="row justify-center q-px-md"
        :class="$q.screen.gt.xs ? 'q-col-gutter-xl' : ''"
        style="max-width: 1100px; margin: 0 auto"
      >
        <div class="col-12 col-sm-6" v-for="report in reports" :key="report.title">
          <q-img :src="report.image" :ratio="16 / 9" class="rounded-borders shadow-3" />
          <div class="report-body q-mt-md text-grey-9">
            <span class="text-weight-bold text-underline">{{ report.title }}</span>
            {{ report.body }}
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup lang="ts">
import effect1 from 'assets/environment/temp.png';
import effect2 from 'assets/environment/wildfire.png';
import effect3 from 'assets/environment/wheat.png';

import data1 from 'assets/environment/data-1.png';
import data2 from 'assets/environment/data-2.png';
import data3 from 'assets/environment/data-3.png';

const effects = [
  {
    image: effect1,
    title: 'Approaching <br> the threshold',
    body: 'The world is dangerously close to crossing the critical 1.5°C warming threshold. The three-year average for 2023 to 2025 sits at 1.48°C above pre-industrial levels, and we are on track to breach the 1.5°C limit within the next decade.',
  },
  {
    image: effect2,
    title: 'Unprecedented <br> Wildfires',
    body: 'Wildfires are now burning twice as much forest as they did 20 years ago. Driven by shifting weather, even historically wet tropical rainforests are beginning to burn.',
  },
  {
    image: effect3,
    title: 'Systemic <br> Disruption',
    body: 'As sea levels rise and weather patterns become increasingly erratic, the ripple effects threaten global food production and the stability of borderless supply chains..',
  },
];

const reports = [
  {
    image: data1,
    title: 'UNEP Emissions Gap Report 2025:',
    body: 'Read the latest findings on shifting weather, wildfire rates, and global emissions.',
  },
  {
    image: data2,
    title: 'PreventionWeb 2025 Report:',
    body: 'Understand the data behind the 1.5°C warming threshold.',
  },
  {
    image: data3,
    title: 'World Resources Institute (WRI):',
    body: 'Explore the economic case for climate adaptation investments.',
  },
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

.gradient-text {
  background: linear-gradient(45deg, #205072, #329d9c);
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
}

.container-2 {
  aspect-ratio: 35 / 9;
  @include mobile {
    aspect-ratio: auto;
  }
}

.effects-section {
  background-image: linear-gradient(135deg, #0a4a6f 0%, #157e9f 50%, #29cbb4 100%);
  aspect-ratio: 25 / 9;
  @include mobile {
    aspect-ratio: auto;
  }
}

.text-underline {
  text-decoration: underline;
  text-decoration-thickness: 1px;
  text-underline-offset: 3px;
}

.tag-title {
  @include mobile {
    font-size: 2.5vw;
    margin-bottom: 10px;
  }
  @include tablet_desktop {
    font-size: clamp(12px, 1.2vw, 16px);
    margin-bottom: 30px;
  }
}

.hero-title {
  @include mobile {
    font-size: 5vw;
    margin-bottom: 10px;
  }
  @include tablet_desktop {
    font-size: clamp(32px, 4vw, 64px);
    margin-bottom: 30px;
  }
}

.hero-subtitle {
  @include mobile {
    font-size: 3vw;
  }
  @include tablet_desktop {
    font-size: clamp(14px, 1.5vw, 20px);
  }
}

.section-title {
  @include mobile {
    font-size: 5vw;
  }
  @include tablet_desktop {
    font-size: clamp(24px, 3.5vw, 48px);
  }
}

.section-body {
  @include mobile {
    font-size: clamp(14px, 2.3vw, 18px);
  }
  @include tablet_desktop {
    font-size: clamp(14px, 1.5vw, 20px);
  }
}

.effect-title {
  line-height: 1.2;
  @include mobile {
    font-size: 4.5vw;
  }
  @include tablet_desktop {
    font-size: clamp(16px, 1.8vw, 24px);
  }
}

.effect-image {
  @include mobile {
    width: clamp(40px, 15vw, 80px);
    height: auto;
  }
  @include tablet_desktop {
    width: clamp(50px, 8vw, 80px);
    height: auto;
  }
}

.effect-body {
  @include mobile {
    font-size: clamp(14px, 2.5vw, 20px);
  }
  @include tablet_desktop {
    font-size: clamp(12px, 1.1vw, 16px);
  }
}

.roi-title {
  @include mobile {
    font-size: 6vw;
  }
  @include tablet_desktop {
    font-size: clamp(28px, 3.5vw, 48px);
  }
}

.roi-body {
  @include mobile {
    font-size: clamp(14px, 2.3vw, 18px);
  }
  @include tablet_desktop {
    font-size: clamp(14px, 1.5vw, 18px);
  }
}

.explore-title {
  @include mobile {
    font-size: 6vw;
    margin-bottom: 10px;
  }
  @include tablet_desktop {
    font-size: clamp(28px, 3.5vw, 48px);
    margin-bottom: 30px;
  }
}

.report-body {
  @include mobile {
    font-size: clamp(14px, 2.3vw, 18px);
  }
  @include tablet_desktop {
    font-size: clamp(14px, 1.2vw, 18px);
  }
}
</style>
