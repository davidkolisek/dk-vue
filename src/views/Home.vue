<template>
  <div class="home">
    <Header
      title="David Kolisek"
      subtitle="Hello, my name is"
      class="main-header-about-gradient"
    />
    <div class="main-container">
      <AboutCards/>
      <h2 class="main-label">My knoweldges</h2>
      <KnowledgeCards/>
      <h2 class="main-label">Frameworks & libraries</h2>
      <FrameworksCards/>
    </div>
  </div>
</template>

<script>
import BaseCard from "../components/cards/BaseCard.vue";
import Header from "../components/layout//Header.vue";
import KnowledgeCards from "./modules/Home/KnowledgeCards.vue";
import FrameworksCards from "./modules/Home/FrameworksCards.vue";
import AboutCards from "./modules/Home/AboutCards.vue";

export default {
  components: {
    BaseCard,
    KnowledgeCards,
    AboutCards,
    FrameworksCards,
    Header,
  },
};
</script>

<style lang="scss" scoped>
.main-container {
  position: relative;
  top: -1.5rem;
}
.main-label{
  margin-top: 2rem;
}
</style>
