<template>
  <div class="main-header">
    <div class="main-container">
      <div class="header-wrapper">
        <div>
          <img src="../../assets/images/me.jpg" alt="" />
        </div>
        <div>
          <span>{{ subtitle }}</span>
          <h1>{{ title }}</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String,
    subtitle: String,
  },
};
</script>

<style lang="scss" scoped>
.main-header {
  border-radius: 30% 70% 78% 22% / 0% 0% 100% 100%;
  max-width: 768px;
  margin: 0 auto;
  .main-container {
    min-height: 130px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    padding-top: 3rem;
    padding-left: 3rem;
    .header-wrapper {
      display: flex;
      flex-direction: row;
      div {
        &:nth-child(1) {
          width: 90px;
          height: 90px;
          border-radius: 52% 48% 37% 63% / 39% 38% 62% 61%;
          overflow: hidden;
          margin-right: 1rem;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
      }
    }
  }
  &-about-gradient {
    background: rgb(235, 179, 80);
    background: linear-gradient(
      215deg,
      rgba(235, 179, 80, 1) 0%,
      rgba(236, 83, 106, 1) 100%
    );
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
  span {
    color: #fff;
    font-weight: 500;
  }
}
</style>
