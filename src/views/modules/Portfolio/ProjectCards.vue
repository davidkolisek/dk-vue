<template>
  <div>
    <h2 class="main-label">Static websites</h2>
    <div class="items-wrapper">
      <div class="overflow-wrapper">
        <ImageBgCard
          v-for="item in staticWebsites"
          :key="item.cardtitle"
          :imageUrl="item.imageUrl"
          :cardtitle="item.cardtitle"
        />
      </div>
    </div>
    <h2 class="main-label">Web applications</h2>
    <div class="items-wrapper">
      <div class="overflow-wrapper">
        <ImageBgCard
          v-for="item in webApps"
          :key="item.cardtitle"
          :imageUrl="item.imageUrl"
          :cardtitle="item.cardtitle"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ImageBgCard from "../../../components/cards/ImageBgCard.vue";

export default {
  name: "ProjectCards",
  components: { ImageBgCard },
  data: function () {
    return {
      staticWebsites: [
        {
          imageUrl: "../../../../src/assets/images/projects/ceko.png",
          cardtitle: "CeKo Interier s.r.o",
        },
        {
          imageUrl:
            "../../../../src/assets/images/projects/mymatch-marketing.png",
          cardtitle: "Mymatch 2021",
        },
        {
          imageUrl: "../../../../src/assets/images/projects/prayogi.png",
          cardtitle: "Prayogi",
        },
        {
          imageUrl: "../../../../src/assets/images/projects/villa.png",
          cardtitle: "Villa perle delamer",
        },
      ],
      webApps: [
        {
          imageUrl: "../../../../src/assets/images/projects/mymatch-app.png",
          cardtitle: "Mymatch 2021 app - Reactjs",
        },
        {
          imageUrl: "../../../../src/assets/images/projects/vedr.png",
          cardtitle: "vedr.sk - weather web app",
        },
        {
          imageUrl: "../../../../src/assets/images/projects/mymatch1.png",
          cardtitle: "Mymatch 2017 - angular",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.items-wrapper{
  width: 100%;
  overflow-x: auto;
  overflow-y: hidden;
}
.overflow-wrapper {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
}
</style>
