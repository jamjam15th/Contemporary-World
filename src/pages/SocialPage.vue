<template>
  <q-page>
    <!-- Hero Section -->
    <q-img src="~assets/Social/social-1.jpg" style="background-color: #2c3e50" :ratio="16 / 9">
      <div class="text-center flex flex-center column full-height full-width" style="background: rgba(0, 0, 0, 0.6);">
        <q-chip
          class="bg-white text-dark text-weight-bold q-mb-md"
          style="font-size: 14px; padding: 16px 24px; border-radius: 24px;"
        >
          Social Media and Digital Culture
        </q-chip>
        <div class="hero-title text-weight-bold q-mb-sm text-white">
          The Global Digital Landscape
        </div>
        <div class="hero-subtitle text-weight-medium text-white q-mt-sm">
          Social media is the nervous system of modern globalization. It instantly dissolves physical borders,<br v-if="$q.screen.width > $q.screen.height" />
          fundamentally altering how billions of people build identities, conduct business, and share information<br v-if="$q.screen.width > $q.screen.height" />
          across the globe.
        </div>
      </div>
    </q-img>

    <!-- Content Sections -->
    <div style="max-width: 1200px; margin: 0 auto; padding-top: 40px; padding-bottom: 40px;">
      
      <!-- Global Interconnectedness -->
      <div class="row items-center q-mt-md" style="margin-bottom: 80px;">
        <div class="col-12 col-md-6 q-pa-md">
          <q-img src="~assets/Social/Interconnectivity.png" style="border-radius: 8px;" />
        </div>
        <div class="col-12 col-md-6 q-pa-md">
          <div :class="$q.screen.width > $q.screen.height ? 'text-left q-pl-xl' : 'text-center'">
            <div class="text-weight-bold text-dark q-mb-md section-title">
              Global Interconnectedness
            </div>
            <div class="text-weight-regular section-body">
              Social media is a dominant force in modern digital culture, enabling the lightning-fast global spread of information, ideas, and cultural trends. Through borderless platforms like Facebook, Instagram, X (Twitter), and TikTok, our global societies have grown more interconnected than ever before.
            </div>
          </div>
        </div>
      </div>

      <!-- The Economic & Identity Engine -->
      <div class="row items-center" style="margin-bottom: 80px;">
        <div class="col-12 col-md-6 q-pa-md" :style="$q.screen.width <= $q.screen.height ? 'order: 2' : 'order: 1'">
          <div :class="$q.screen.width > $q.screen.height ? 'text-left q-pr-xl' : 'text-center'">
            <div class="text-weight-bold text-dark q-mb-md section-title">
              The Economic & Identity Engine
            </div>
            <div class="text-weight-regular section-body">
              Beyond socializing, these networks function as powerful communication and economic tools. Individuals and organizations leverage them globally for personal branding, targeted marketing, and cross-border audience engagement—fundamentally reshaping modern business and individual identity formation.
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 q-pa-md" :style="$q.screen.width <= $q.screen.height ? 'order: 1' : 'order: 2'">
          <q-img src="~assets/Social/socializing.jpg" style="border-radius: 8px;" />
        </div>
      </div>

      <!-- The Systemic Challenges -->
      <div class="row items-center" style="margin-bottom: 80px;">
        <div class="col-12 col-md-6 q-pa-md">
          <q-img src="~assets/Social/SocialChallenge.png" style="border-radius: 8px;" />
        </div>
        <div class="col-12 col-md-6 q-pa-md">
          <div :class="$q.screen.width > $q.screen.height ? 'text-left q-pl-xl' : 'text-center'">
            <div class="text-weight-bold text-dark q-mb-md section-title">
              The Systemic Challenges
            </div>
            <div class="text-weight-regular section-body">
              With massive scale comes massive complexity. Social media raises critical global challenges surrounding content moderation, the viral spread of misinformation, and the protection of free expression. It has evolved into a complex ecosystem that actively shapes social, political, and cultural dynamics worldwide.
            </div>
          </div>
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
    font-size: 6vw;
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
