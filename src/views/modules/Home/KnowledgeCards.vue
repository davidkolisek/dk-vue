<template>
  <div>
    <div class="main-row">
      <div class="main-col">
        <SkillCard cardtitle="HTML" cardSubtitle="95%"></SkillCard>
      </div>
      <div class="main-col">
        <SkillCard cardtitle="CSS" cardSubtitle="90%"></SkillCard>
      </div>
      <div class="main-col">
        <SkillCard cardtitle="Javascript" cardSubtitle="70%"></SkillCard>
      </div>
      <div class="main-col">
        <SkillCard cardtitle="Sass" cardSubtitle="80%"></SkillCard>
      </div>
      <div class="main-col">
        <SkillCard cardtitle="Typescript" cardSubtitle="50%"></SkillCard>
      </div>
    </div>
  </div>
</template>

<script>
import SkillCard from "../../../components/cards/SkillCard.vue";
export default {
  name: "KnowledgeCards",
  components: {
    SkillCard,
  },
};
</script>

<style lang="scss" scoped>
//row1
$html: linear-gradient(
  215deg,
  rgba(242, 101, 36, 1) 0%,
  rgba(221, 75, 37, 1) 100%
);
$css: linear-gradient(
  94deg,
  rgba(59, 154, 218, 1) 0%,
  rgba(113, 178, 222, 1) 100%
);
$js: linear-gradient(
  94deg,
  rgba(221, 193, 48, 1) 0%,
  rgba(242, 211, 35, 1) 100%
);
//row2
$ts: #2f72bb;
$sass: #cf659a;
.main-row {
  flex-wrap: wrap;
  &:nth-child(1) {
    .main-col {
      .skill-card {
        margin-bottom: 0;
      }
      &:nth-child(1) {
        .skill-card {
          background: $html;
        }
      }
      &:nth-child(2) {
        .skill-card {
          background: $css;
        }
      }
      &:nth-child(3) {
        .skill-card {
          background: $js;
        }
      }
      &:nth-child(4) {
        .skill-card {
          background: $sass;
        }
      }
      &:nth-child(5) {
        .skill-card {
          background: $ts;
        }
      }
    }
  }
}
</style>
