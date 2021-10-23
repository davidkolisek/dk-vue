<template>
  <div class="base-card">
    <h3>{{cardtitle}}</h3>
    <span>{{cardSubtitle}}</span>
    <slot/>
  </div>
</template>

<script>
export default {
  name: "BaseCard",
  props: {
    cardtitle: String,
    cardSubtitle: String
  }
};
</script>

<style lang="scss" scoped>
.base-card {
  background: #fff;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 5px 15px 0px;
  padding: 1rem;
  border-radius: 12px;
  margin-bottom: 1rem;
  h3{
    font-size: 1.5rem;
    color: #eb5f67;
    margin: 0 0 .5rem;
  }
  span {
    font-size: .8rem;
    color: #999;
    line-height: 1.75;
  }
}
</style>
