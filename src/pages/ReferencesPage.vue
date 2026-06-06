<template>
  <q-page class="bg-white flex flex-center q-pa-md">
    <div class="references-container full-width">

      <div class="references-title text-weight-bold text-center q-mb-xl">
        References
      </div>

      <div class="references-list text-grey-9">
        <p
          v-for="(ref, index) in references"
          :key="index"
          class="hanging-indent"
          v-html="ref"
        ></p>
      </div>

    </div>
  </q-page>
</template>

<script setup lang="ts">
// All provided citations are stored here for clean template rendering
const references = [
  'Brandon, C., Kratzer, B., Aggarwal, A., Heubaum, H., & Novenario, C. (2025, June 3). The compelling investment case for climate adaptation. World Resources Institute. <br> <a href="https://www.wri.org/insights/climate-adaptation-investment-case" target="_blank" rel="noopener noreferrer">https://www.wri.org/insights/climate-adaptation-investment-case</a>',
  'Brookings Institution. (2020). [Photograph of event/people]. <br> <a href="https://www.brookings.edu/wp-content/uploads/2020/08/2020-08-28T122417Z_997883661_MT1SIPA000OIQH12_RTRMADP_3_SIPA-USA.jpg" target="_blank" rel="noopener noreferrer">https://www.brookings.edu/wp-content/uploads/2020/08/2020-08-28T122417Z_997883661_MT1SIPA000OIQH12_RTRMADP_3_SIPA-USA.jpg</a>', 
  'Dreamstime. (n.d.). United Nations General Assembly Hall [Photograph]. <br> <a href="https://www.dreamstime.com/stock-images-united-nations-general-assembly-hall-image19215934" target="_blank" rel="noopener noreferrer">https://www.dreamstime.com/stock-images-united-nations-general-assembly-hall-image19215934</a>',
  `Ossa, R., Nee, C., D'Andrea Adrian, B., Bekkers, E., Blanga-Gubbay, M., Auboin, M., World Trade Organization, & Information and External Relations Division. (2025). Global trade outlook and statistics. World Trade Organization. <br> <a href="https://www.wto.org/english/res_e/booksp_e/trade_outlook25_e.pdf" target="_blank" rel="noopener noreferrer">https://www.wto.org/english/res_e/booksp_e/trade_outlook25_e.pdf</a>`,  
  'Science and Development Network. (2026, January 22). World on track to breach 1.5C target by 2030. PreventionWeb. <br> <a href="https://www.preventionweb.net/news/world-track-breach-15c-target-2030" target="_blank" rel="noopener noreferrer">https://www.preventionweb.net/news/world-track-breach-15c-target-2030</a>',
  'Slotta, D. (2025, December 17). Social media - statistics & facts. Statista. Retrieved June 6, 2026, from <br> <a href="https://www.statista.com/topics/1164/social-networks/" target="_blank" rel="noopener noreferrer">https://www.statista.com/topics/1164/social-networks/</a>',
  'UN Trade and Development. (2022, December 13). Global trade set to hit record $32 trillion in 2022, but outlook increasingly gloomy for 2023. <br> <a href="https://unctad.org/news/global-trade-set-hit-record-32-trillion-2022-outlook-increasingly-gloomy-2033" target="_blank" rel="noopener noreferrer">https://unctad.org/news/global-trade-set-hit-record-32-trillion-2022-outlook-increasingly-gloomy-2033</a>',
  'United Nations. (n.d.). Human rights. Retrieved June 6, 2026, from <br> <a href="https://www.un.org/en/global-issues/human-rights" target="_blank" rel="noopener noreferrer">https://www.un.org/en/global-issues/human-rights</a>',
  'United Nations Environment Programme. (2025). Emissions gap report 2025: Off target—Continued collective inaction puts global temperature goal at risk. <br> <a href="https://www.unep.org/resources/emissions-gap-report-2025" target="_blank" rel="noopener noreferrer">https://www.unep.org/resources/emissions-gap-report-2025</a>',
  'United Nations High Commissioner for Refugees. (n.d.). Mid-year trends. Retrieved June 6, 2026, from <br> <a href="https://www.unhcr.org/mid-year-trends-0" target="_blank" rel="noopener noreferrer">https://www.unhcr.org/mid-year-trends-0</a>',
  'United Nations High Commissioner for Refugees. (2025a). Mid-year trends 2025. <br> <a href="https://www.unhcr.org/media/mid-year-trends-2025" target="_blank" rel="noopener noreferrer">https://www.unhcr.org/media/mid-year-trends-2025</a>',
  'United Nations High Commissioner for Refugees. (2025b, November 4). Mid-year trends. <br> <a href="https://www.unhcr.org/mid-year-trends" target="_blank" rel="noopener noreferrer">https://www.unhcr.org/mid-year-trends</a>',
  'United Nations High Commissioner for Refugees. (2025c, November 10). UNHCR report reveals extreme weather driving repeated displacement among conflict-affected communities [Press release]. <br> <a href="https://www.unhcr.org/news/press-releases/unhcr-report-reveals-extreme-weather-driving-repeated-displacement-among" target="_blank" rel="noopener noreferrer">https://www.unhcr.org/news/press-releases/unhcr-report-reveals-extreme-weather-driving-repeated-displacement-among</a>',
  'World Economic Forum, & PwC. (2019). The impact of 5G: Creating new value across industries and society [Report]. <br> <a href="https://www3.weforum.org/docs/WEF_The_Impact_of_5G.pdf" target="_blank" rel="noopener noreferrer">https://www3.weforum.org/docs/WEF_The_Impact_of_5G.pdf</a>',
  'World Trade Organization. (2025a). World trade report 2025: Making trade and AI work together to the benefit of all. <br> <a href="https://www.wto.org/english/res_e/publications_e/wtr25_e.htm" target="_blank" rel="noopener noreferrer">https://www.wto.org/english/res_e/publications_e/wtr25_e.htm</a>',
  'World Trade Organization. (2025b, October 7). AI goods and frontloading lift world trade in 2025 but outlook dims for 2026. <br> <a href="https://www.wto.org/english/news_e/news25_e/stat_07oct25_e.htm" target="_blank" rel="noopener noreferrer">https://www.wto.org/english/news_e/news25_e/stat_07oct25_e.htm</a>',
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
  padding-left: 2rem;
  text-indent: -2rem;

  margin-bottom: 1.2rem;
  line-height: 1.6;
  font-size: clamp(12px, 1.2vw, 16px);

  word-wrap: break-word;
  overflow-wrap: break-word;
}

.hanging-indent :deep(a) {
  color: #3b8e96; 
  text-decoration: none;
  word-break: break-all;
}
</style>
