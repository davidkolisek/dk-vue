<template>
  <nav class="main-nav">
    <router-link to="/"
      ><i class="icon-person"></i><span>Home</span></router-link
    >
    <router-link to="/portfolio"
      ><i class="icon-grid"></i><span>Portfolio</span></router-link
    >
    <router-link to="/pricing"
      ><i class="icon-money"></i><span>Pricing</span></router-link
    >
    <router-link to="/contact"
      ><i class="icon-mail"></i><span>Contact</span></router-link
    >
  </nav>
</template>

<script>
export default {
  name: "Navigation",
};
</script>

<style lang="scss" scoped>
.main-nav {
  box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
  position: fixed;
  bottom: 0;
  padding: 0.5rem 0.25rem;
  left: 0;
  right: 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  background: #fff;
  @media (min-width: 576px) {
    max-width: 320px;
    left: calc(50% - 160px);
    padding: 0.75rem;
  }
  a {
    text-decoration: none;
    width: 100%;
    padding: 0.5rem;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    border-radius: 12px;
    i {
      color: #767676;
      font-size: 1.5rem;
      @media (max-width: 576px) {
        font-size: 1.25rem;
      }
    }
    span {
      max-width: 0;
      overflow: hidden;
      position: relative;
      @media (max-width: 576px) {
        font-size: 0.8rem;
      }
    }
    &.router-link-active {
      background-color: #ffeeef;
      i {
        color: #ec6266;
      }
      span {
        transition: max-width ease 350ms;
        max-width: 100px;
        display: block;
        margin-left: 0.25rem;
        color: #ec6266;
        font-weight: 600;
      }
    }
  }
}
</style>
