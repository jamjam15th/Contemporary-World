<template>
  <q-page>
    <!-- Hero Section -->
    <q-img src="~assets/landing.png" :ratio="16 / 9">
      <div class="text-center flex flex-center column bg-transparent full-height full-width">
        <div class="hero-title text-weight-bold q-mb-sm">Globalization</div>
        <div class="hero-subtitle text-weight-medium">
          <div>
            It's how the world's economies, cultures, and populations have grown
            <br v-if="$q.screen.width > $q.screen.height" />
            increasingly tangled with one another.
          </div>
        </div>
        <div class="q-mt-xl q-gutter-x-md">
          <q-btn label="Overview" no-caps rounded class="custom-button" @click="navigateTo('#overview')" />
          <q-btn label="View effects" no-caps rounded class="custom-button" @click="navigateTo('#effects')" />
        </div>
      </div>
    </q-img>

    <!-- Connecting Section -->
    <div class="row flex flex-center q-mt-lg q-mt-xl-md">
      <div class="col-6">
        <q-img src="~assets/landing-2.png" />
      </div>
      <div
        class="col-12 col-sm-6"
        :class="$q.screen.width > $q.screen.height ? 'text-left q-pa-xl' : ' text-center q-pa-md '"
      >
        <div class="connecting-title">Connecting</div>
        <div class="connecting-title text-weight-bold">the Civilization</div>
        <div class="connecting-body text-weight-medium q-mt-md">
          Trade and technology are the main drivers, and the ripple effects touch everything from
          how local economies function, to how governments make decisions, to whether people's basic
          rights are actually protected.
        </div>
      </div>
    </div>

    <!-- Overview Section -->
    <q-img id="overview" src="~assets/landing-3.png" :ratio="16 / 9" class="q-mt-lg">
      <div
        class="text-left justify-center column absolute-full bg-transparent"
        :class="$q.screen.width > $q.screen.height ? 'q-ml-xl' : 'q-pa-md'"
      >
        <div class="row">
          <div class="col-9 col-sm-8 col-md-7">
            <div class="overview-title text-weight-bold q-mb-md">Overview about Globalization</div>
            <div class="overview-body q-mb-sm">
              Global trade in goods and services reached $32 trillion in 2022, with the UN Trade and
              Development agency warning of tougher conditions ahead. That figure alone shows how
              deeply interconnected global economies have become.
            </div>
            <div class="overview-body q-mb-sm">
              Globalization isn't just about breaking into new markets anymore. It's about keeping
              up with political shifts, digital disruption, and consumers who expect more, faster.
            </div>
            <div class="overview-body q-mb-sm">
              The WTO revised its 2025 global trade forecast upward to 2.4% growth, driven largely
              by booming demand for AI-related goods like semiconductors, servers, and
              telecommunications equipment, which accounted for nearly half of all merchandise trade
              expansion in the first half of the year.
            </div>
          </div>
        </div>
      </div>
    </q-img>

    <!-- Effects Section -->
    <div
      id="effects"
      class="row justify-center"
      :class="$q.screen.width > $q.screen.height ? 'q-pa-xl' : 'q-pa-md'"
    >
      <div class="col-12 col-lg-11">
        <div :class="$q.screen.width > $q.screen.height ? 'q-mb-xl' : 'text-center'">
          <div class="effects-header text-weight-bolder text-grey-10 q-mb-sm">
            The Effects of Globalization
          </div>
          <div class="effects-subtitle text-weight-regular text-grey-8">
            Globalization has led to increases in standards of living around the world, but not all
            of its effects are positive for everyone.
          </div>
        </div>

        <div class="row q-col-gutter-lg q-mt-md">
          <div class="col-12 col-lg-3" v-for="effect in effects" :key="effect.title">
            <div class="row no-wrap q-gutter-sm">
              <q-icon
                :name="effect.icon"
                :color="effect.color"
                :size="
                  $q.screen.lt.sm ? 'sm' : $q.screen.md ? '60px' : $q.screen.lt.md ? 'xl' : 'lg'
                "
              />
              <div class="col">
                <div class="text-primary text-weight-bold effect-title">
                  {{ effect.title }}
                </div>
                <div class="effect-body q-mt-md">
                  {{ effect.body }}
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup lang="ts">
const navigateTo = (path: string) => {
  // Handle hash-based navigation (for sections on same page)
  if (path.startsWith('#')) {
    const target = document.querySelector(path);
    if (target) {
      target.scrollIntoView({ behavior: 'smooth' });
    }
  } else {
    // Handle regular navigation
    window.location.href = path;
  }

};

const effects = [
  {
    icon: 'check_circle_outline',
    color: 'positive',
    title: 'Trade and job creation have raised living standards',
    body: "More trade and job creation have raised living standards for a real number of people. Globalization rewired the global economy in ways that opened doors that didn't exist before.",
  },
  {
    icon: 'check_circle_outline',
    color: 'positive',
    title: 'Given individuals and communities economic ground to stand on',
    body: "It's also given individuals and communities economic ground to stand on, letting them preserve their cultural identity. Traditional crafts and art forms, for example, now reach buyers worldwide through online platforms.",
  },
  {
    icon: 'highlight_off',
    color: 'negative',
    title: 'Cultural homogenization is quietly eroding what makes local communities distinct',
    body: 'Critics argue that cultural homogenization is quietly eroding what makes local communities distinct, and that ceding control over critical technologies leaves nations vulnerable, both economically and in terms of security.',
  },
  {
    icon: 'highlight_off',
    color: 'negative',
    title: 'A widening gap',
    body: 'Research also points to a widening gap: globalization tends to benefit the highly educated while putting downward pressure on wages for workers without specialized skills.',
  },
];
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

.overview-title {
  @include portrait {
    font-size: 4vw;
  }
  @include landscape {
    font-size: 3.5vw;
  }
}

.overview-body {
  @include portrait {
    font-size: clamp(8px, 1.7vw, 18px);
  }
  @include landscape {
    font-size: 1.2vw;
  }
}

.effects-header {
  @include portrait {
    font-size: 5vw;
  }
  @include landscape {
    font-size: 3.5vw;
  }
}

.effects-subtitle {
  @include portrait {
    font-size: 3vw;
  }
  @include landscape {
    font-size: 1.5vw;
  }
}

.effect-title {
  line-height: 1.5;
  @include portrait {
    font-size: 4vw;
  }
  @include landscape {
    font-size: 1.6vw;
  }
}

.effect-body {
  @include portrait {
    font-size: 3vw;
  }
  @include landscape {
    font-size: 1.1vw;
  }
}
</style>
