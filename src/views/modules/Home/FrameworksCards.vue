<template>
  <div class="list-wrapper">
    <ListItemCard
      v-for="item in items"
      :key="item.title"
      :title="item.title"
      :subtitle="item.subtitle"
      :skillRate="item.skillRate"
      :logoUrl="item.logoUrl"
    />
  </div>
  <div class="btn-wrapper">
    <button class="toggle-show-hide" @click="toggleShow"></button>
  </div>
</template>

<script>
import ListItemCard from "../../../components/cards/ListItemCard.vue";
export default {
  name: "FrameworksCards",
  components: {
    ListItemCard,
  },
  data: function () {
    return {
      showMore: Boolean,
      items: [
        {
          title: "Bootstrap",
          subtitle: "version 3,4,5",
          skillRate: "95%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/b/b2/Bootstrap_logo.svg/512px-Bootstrap_logo.svg.png",
        },
        {
          title: "Material UI",
          subtitle: "Used for build webapps in react",
          skillRate: "90%",
          logoUrl: "https://cdn.worldvectorlogo.com/logos/material-ui-1.svg",
        },
        {
          title: "Native base",
          subtitle: "For build a mobile app in React",
          skillRate: "80%",
          logoUrl: "https://docs.nativebase.io/img/nativebaselogo.svg",
        },
        {
          title: "React.js",
          subtitle: "My most used framework",
          skillRate: "70%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1280px-React-icon.svg.png",
        },
        {
          title: "React Native",
          subtitle: "Only a few times but i know the bases :)",
          skillRate: "50%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1280px-React-icon.svg.png",
        },
        {
          title: "Vue.js",
          subtitle: "Only a few times but i know the bases :)",
          skillRate: "25%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1184px-Vue.js_Logo_2.svg.png",
        },
        {
          title: "Firebase",
          subtitle: "For backend purposes in mobile/web apps",
          skillRate: "45%",
          logoUrl:
            "https://cdn.dribbble.com/users/528264/screenshots/3140440/media/5f34fd1aa2ebfaf2cd548bafeb021c8f.png?compress=1&resize=400x300",
        },
        {
          title: "GraphQL/Apollo server",
          subtitle: "Using only few times",
          skillRate: "20%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/GraphQL_Logo.svg/2048px-GraphQL_Logo.svg.png",
        },
        {
          title: "Angular",
          subtitle: "I was using only angular 2,4",
          skillRate: "25%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Angular_full_color_logo.svg/2048px-Angular_full_color_logo.svg.png",
        },
        {
          title: "Wordpress",
          subtitle: "Using only few times",
          skillRate: "40%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/9/98/WordPress_blue_logo.svg/1024px-WordPress_blue_logo.svg.png",
        },
        {
          title: "Laravel",
          subtitle: "Using only few times",
          skillRate: "30%",
          logoUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Laravel.svg/1969px-Laravel.svg.png",
        },
        {
          title: "Symfony",
          subtitle: "Using only few times",
          skillRate: "30%",
          logoUrl: "https://image.pngaaa.com/889/142889-middle.png",
        },
      ],
    };
  },
  methods: {
    toggleShow() {
      let wrapper = document.querySelector(".list-wrapper");
      let btn = document.querySelector(".toggle-show-hide");
      wrapper.classList.toggle("show-all");
      btn.classList.toggle("collapsed");
      // setTimeout(() => {
      //   window.scrollTo(0, document.body.scrollHeight);
      //   console.log(2)
      // }, 150);
    },
  },
};
</script>

<style lang="scss" scoped>
.list-wrapper {
  max-height: 500px;
  transition: all ease 250ms;
  overflow: hidden;

  .list-item-card {
    display: none;
    &:nth-child(-n + 3) {
      display: flex;
    }
  }
  &.show-all {
    max-height: 1200px;
    /* animation: showHide 1s; */
    transition: all ease 250ms;
    .list-item-card {
      display: flex;
    }
    .toggle-show-hide {
      cursor: pointer;
      background: linear-gradient(
        215deg,
        rgba(235, 179, 80, 1) 0%,
        rgba(236, 83, 106, 1) 100%
      );
      border: none;
      width: 36px;
      height: 36px;
      border-radius: 99px;
      color: #fff;
      text-align: center;
      margin: 0 auto;
      position: relative;
    }
  }
}
.list-item-card {
  margin-bottom: 1rem;
}
.btn-wrapper {
  margin: 0 auto;
  text-align: center;
}
.toggle-show-hide {
  cursor: pointer;
  transition: all ease 250ms;
  background: linear-gradient(
    215deg,
    rgba(235, 179, 80, 1) 0%,
    rgba(236, 83, 106, 1) 100%
  );
  border: none;
  width: 36px;
  height: 36px;
  border-radius: 99px;
  color: #fff;
  text-align: center;
  margin: 0 auto;
  position: relative;
  &:before {
    transition: all ease 250ms;
    content: "";
    position: absolute;
    width: 15px;
    height: 2px;
    left: 6px;
    bottom: 17px;
    transform: rotate(45deg);
    background-color: #fff;
  }
  &:after {
    transition: all ease 250ms;
    content: "";
    position: absolute;
    width: 15px;
    height: 2px;
    right: 6px;
    bottom: 17px;
    transform: rotate(-45deg);
    background-color: #fff;
  }
  &.collapsed {
    &:before {
      transition: all ease 250ms;
      content: "";
      position: absolute;
      width: 15px;
      height: 2px;
      left: 6px;
      bottom: 17px;
      transform: rotate(-45deg);
      background-color: #fff;
    }
    &:after {
      transition: all ease 250ms;
      content: "";
      position: absolute;
      width: 15px;
      height: 2px;
      right: 6px;
      bottom: 17px;
      transform: rotate(45deg);
      background-color: #fff;
    }
  }
}
</style>
