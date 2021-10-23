<template>
  <div class="skill-card">
    <h3>{{cardtitle}}</h3>
    <span>{{cardSubtitle}}</span>
  </div>
</template>

<script>
export default {
  name: "SkillCard",
  props: {
    cardtitle: String,
    cardSubtitle: String
  }
};
</script>

<style lang="scss" scoped>
.skill-card {
  background: #fff;
  padding: .75rem 1rem .5rem 1rem;
  border-radius: 12px;
  h3{
    font-size: .9rem;
    color: #fff;
    margin: 0 0 .5rem;
  }
  span {
    font-size: 1.5rem;
    color: #fff;
    font-weight: 700;
    line-height: 1.75;
  }
}
</style>
