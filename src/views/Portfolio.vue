<template>
  <div class="portfolio">
    <HeaderSubpage title="Portfolio" class="main-header-portfolio-gradient" />
    <div class="main-container">
      <BaseCard
        class="no-h3"
        cardSubtitle="I have been working on websites and web applications for more than 5 years. The work on the website ends for me, when I see green numbers in Lighthouse, the website is sufficiently tested on all devices and deployed on the required domain."
      ></BaseCard>
      <ProjectCards />
    </div>
  </div>
</template>

<script>
import BaseCard from "../components/cards/BaseCard.vue";
import HeaderSubpage from "../components/layout//HeaderSubpage.vue";
import ProjectCards from "./modules/Portfolio/ProjectCards.vue";
import FrameworksCards from "./modules/Portfolio/ProjectCards.vue";

export default {
  components: {
    ProjectCards,
    BaseCard,
    HeaderSubpage,
    FrameworksCards,
  },
};
</script>

<style lang="scss" scoped>
.main-container {
  position: relative;
  top: -1.5rem;
}
</style>
