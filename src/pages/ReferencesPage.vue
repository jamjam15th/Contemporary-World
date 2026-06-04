<template>
  <q-page class="bg-white flex flex-center q-pa-md">
    <div class="references-container full-width">

      <!-- Title -->
      <div class="references-title text-weight-bold text-center q-mb-xl">
        References
      </div>

      <!-- References List with Hanging Indent -->
      <div class="references-list text-grey-9">
        <p
          v-for="(ref, index) in references"
          :key="index"
          class="hanging-indent"
        >
          {{ ref }}
        </p>
      </div>

    </div>
  </q-page>
</template>

<script setup lang="ts">
// All provided citations are stored here for clean template rendering
const references = [
  "Brookings Institution. (2020). [Photograph of event/people] [Photograph]. Brookings. https://www.brookings.edu/wp-content/uploads/2020/08/2020-08-28T122417Z_997883661_MT1SIPA000OIQH12_RTRMADP_3_SIPA-USA.jpg",
  "Dreamstime. (n.d.). United Nations General Assembly Hall [Photograph]. https://www.dreamstime.com/stock-images-united-nations-general-assembly-hall-image19215934",
  "PreventionWeb. (2025). World on track to breach 1.5C target by 2030. https://www.preventionweb.net/news/world-track-breach-15c-target-2030",
  "Statista. (n.d.). Social networks. https://www.statista.com/topics/1164/social-networks/",
  "United Nations. (n.d.). Human rights. https://www.un.org/en/global-issues/human-rights",
  "United Nations Conference on Trade and Development. (2023). Global trade set to hit record $32 trillion in 2022, but outlook increasingly gloomy for 2023. https://unctad.org/news/global-trade-set-hit-record-32-trillion-2022-outlook-increasingly-gloomy-2023",
  "United Nations Environment Programme. (2025). Emissions gap report 2025. https://www.unep.org/resources/emissions-gap-report-2025",
  "United Nations High Commissioner for Refugees. (n.d.). UNHCR report reveals extreme weather driving repeated displacement among communities. https://www.unhcr.org/news/press-releases/unhcr-report-reveals-extreme-weather-driving-repeated-displacement-among",
  "United Nations High Commissioner for Refugees. (2025a). Mid-year trends. https://www.unhcr.org/mid-year-trends",
  "United Nations High Commissioner for Refugees. (2025b). Mid-year trends 2025. https://www.unhcr.org/media/mid-year-trends-2025",
  "United Nations High Commissioner for Refugees. (2025c, November 4). Mid-year trends. https://www.unhcr.org/mid-year-trends-0",
  "World Resources Institute. (n.d.). Climate adaptation investment case. https://www.wri.org/insights/climate-adaptation-investment-case",
  "World Trade Organization. (2025a). Trade outlook 2025. https://www.wto.org/english/res_e/booksp_e/trade_outlook25_e.pdf",
  "World Trade Organization. (2025b). World trade report 2025. https://www.wto.org/english/res_e/publications_e/wtr25_e.htm",
  "World Trade Organization. (2025c, October 7). News and statistics. https://www.wto.org/english/news_e/news25_e/stat_07oct25_e.htm"
];
</script>

<style scoped lang="scss">
.references-container {
  max-width: 900px; /* Constrains the width so it looks centered like your mockup */
  margin: 0 auto;
  padding: 60px 0;
}

.references-title {
  color: #3b8e96; /* Matches the teal color from the mockup */
  font-size: clamp(32px, 4vw, 48px);
  margin-bottom: clamp(30px, 4vw, 50px);
}

.references-list {
  text-align: left;
}

.hanging-indent {
  /* This creates the APA standard hanging indent */
  padding-left: 2rem;
  text-indent: -2rem;

  margin-bottom: 1.2rem;
  line-height: 1.6;
  font-size: clamp(12px, 1.2vw, 16px);

  /* Critical for long URLs so they don't break the layout on mobile */
  word-wrap: break-word;
  overflow-wrap: break-word;
}
</style>
