<template>
  <BaseCard
    cardtitle="Frontend developer"
    cardSubtitle="I have been working on websites and web applications for more than 5 years. The work on the website ends for me, when I see green numbers in Lighthouse, the website is sufficiently tested on all devices and deployed on the required domain."
    class="carousel-card"
  ></BaseCard>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
import BaseCard from "../../../components/cards/BaseCard.vue";
export default {
  name: "AboutCards",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
    BaseCard,
  },
};
</script>

<style lang="scss" scoped>
.carousel-card {
  margin: 0 auto 1rem;
}
</style>
