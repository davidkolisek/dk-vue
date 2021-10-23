<template>
  <div class="list-item-card">
    <div class="logo-wrapper">
      <img v-bind:src="logoUrl" v-bind:alt="title" />
    </div>
    <div class="text-content">
      <h3>{{ title }}</h3>
      <span>{{ subtitle }}</span>
    </div>
    <span>{{ skillRate }}</span>
  </div>
</template>

<script>
export default {
  name: "ListItemCard",
  props: {
    title: String,
    subtitle: String,
    logoUrl: String,
    skillRate: String,
  },
};
</script>

<style lang="scss" scoped>
.list-item-card {
  background: #fff;
  padding: .5rem;
  border-radius: 12px;
  display: flex;
  flex-direction: row;
  border: 1px solid #eee;
  justify-content: center;
  align-items: center;
  .logo-wrapper{
    width: 50px;
    height: 50px;
    overflow: hidden;
    margin-right: 1rem;
    border-radius: 12px;
    padding: .25rem;
    background-color: #eee;
    img{
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  .text-content {
    flex: 1;
    h3 {
      font-size: 1.1rem;
      color: #272727;
      margin: 0 ;
    }
    span {
      font-size: 0.8rem;
      color: #999;
      font-weight: normal;
    }
  }
  span {
    font-size: 1.5rem;
    color: #272727;
    font-weight: 700;
    line-height: 1.75;
  }
}
</style>
