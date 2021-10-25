<template>
  <div class="base-image-card">
    <img v-bind:src="imageUrl" v-bind:alt="cardtitle" />
    <h3>{{ cardtitle }}</h3>
  </div>
</template>

<script>
export default {
  name: "ImageBgCard",
  props: {
    cardtitle: String,
    imageUrl: String,
  },
};
</script>

<style lang="scss" scoped>
.base-image-card {
  background: #fff;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 5px 15px 0px;
  border-radius: 12px;
  margin-bottom: 1rem;
  overflow: hidden;
  max-height: 250px;
  width: 200px;
  min-width: 200px;
  margin-right: 1rem;
  position: relative;
  &:last-child {
    margin-right: 0;
  }
  &:before {
      transition: all ease 150ms;
    content: "";
    background: linear-gradient(0deg, rgba(0,0,0, .5) 0%, rgba(255, 255, 255, 0) 100%);
    position: absolute;
    bottom: 0px;
    left: 0px;
    right: 0px;
    top: 0;
    z-index: 2;
  }
  &:hover{
    img{
      transition: all ease 150ms;
      transform: scale(1.05,1.05)
    }
  &:before {
      transition: all ease 150ms;
    content: "";
    background: linear-gradient(0deg, rgba(0,0,0, .7) 0%, rgba(255, 255, 255, 0) 100%);
    position: absolute;
    bottom: 0px;
    left: 0px;
    right: 0px;
    top: 0;
    z-index: 2;
  }
  }
  img {
      transition: all ease 150ms;
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: relative;
    z-index: 1;
  }
  h3 {
    font-size: 0.8rem;
    color: #fff;
    position: absolute;
    line-height: 1.75;
    z-index: 3;
    bottom: 0;
    left: 1rem;
  }
}
</style>
