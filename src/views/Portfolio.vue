<template>
  <div class="portfolio">
    <HeaderSubpage title="Portfolio" class="main-header-portfolio-gradient" />
    <div class="main-container">
      <BaseCard
        class="no-h3"
        cardSubtitle="I have been working on websites and web applications for more than 5 years. The work on the website ends for me, when I see green numbers in Lighthouse, the website is sufficiently tested on all devices and deployed on the required domain."
      ></BaseCard>
      <h2 class="main-label">My knoweldges</h2>
    </div>
  </div>
</template>

<script>
import BaseCard from "../components/cards/BaseCard.vue";
import HeaderSubpage from "../components/layout//HeaderSubpage.vue";
import KnowledgeCards from "./modules/Home/KnowledgeCards.vue";
import FrameworksCards from "./modules/Home/FrameworksCards.vue";
import AboutCards from "./modules/Home/AboutCards.vue";

export default {
  components: {
    BaseCard,
    KnowledgeCards,
    AboutCards,
    FrameworksCards,
    HeaderSubpage,
  },
};
</script>

<style lang="scss" scoped>
.main-container {
  position: relative;
  top: -1.5rem;
}
</style>
