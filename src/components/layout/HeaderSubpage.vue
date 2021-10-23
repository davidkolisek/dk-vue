<template>
  <div class="main-header">
    <div class="main-container">
      <div class="header-wrapper">
        <div>
          <h1>{{ title }}</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderSubpage",
  props: {
    title: String,
  },
};
</script>

<style lang="scss" scoped>
.main-header {
  /* border-radius: 30% 70% 78% 22% / 0% 0% 100% 100%; */
  max-width: 768px;
  margin: 0 auto;
  .main-container {
    min-height: 70px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 0rem 0 1.5rem 3rem;
  }
  &-portfolio-gradient {
    transition: all ease 250ms;
    background: linear-gradient(
      94deg,
      rgb(59, 154, 218) 0%,
      rgb(113, 178, 222) 100%
    );
  }
  &-pricing-gradient {
  }
  &-contact-gradient {
  }
  h1 {
    font-weight: 300;
    color: #fff;
    margin: 0 0 1rem 0;
  }
}
</style>
