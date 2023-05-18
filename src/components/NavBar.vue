<template>
  <v-container fluid class="bckg">
    <header :class="{ 'scrolled-nav': scrollPosition }">
      <nav class="my-3">
        <div v-show="!mobile" class="navigation">
          <div class="branding">
            <LogoIcon class="logo-header"/>
          </div>
          <ul class="navigation__list">
            <li><a href="#mission" class="menu-item">Mission</a></li>
            <li><a href="#solution" class="menu-item">Solution</a></li>
            <li><a href="#ecosystem" class="menu-item">Ecosystem</a></li>
            <li><a href="#team" class="menu-item">Team</a></li>
            <li><a href="#roadmap" class="menu-item">Roadmap</a></li>
          </ul>
          <div class="btns-wrapper">
            <a href="https://nft.blockaids.world/" target="_blank" class="btn-main btn-main-collections">NFT
              Collection</a>
            <PopupForm/>
          </div>

        </div>
        <LogoIcon class="logo-header" v-show="mobile"/>
        <!--        <v-spacer></v-spacer>-->
        <div class="icon">
          <MenuIcon
            @click.native="toggleMobileNav"
            v-show="mobile"
            class="menu-icon"
            :class="{ 'icon-active': mobileNav }"
            width="30"
          />
        </div>

        <transition name="mobile-nav">
          <div v-show="mobileNav" class="dropdown-nav text-center">
            <ul>
              <li><a to="#" class="menu-item">About</a></li>
              <li><a to="#" class="menu-item">Business model</a></li>
              <li><a to="#" class="menu-item">Team </a></li>
              <li><a to="#" class="menu-item">Roadmap</a></li>
              <li><a class="menu-item">PitchDeck</a></li>
            </ul>
            <PopupForm/>
            <a href="https://nft.blockaids.online/" target="_blank" class="btn-main btn-main-collections">NFT
              Collection</a>
          </div>
        </transition>
      </nav>
    </header>
  </v-container>
</template>

<script>
import LogoIcon from "./icons/LogoIcon.vue";
import MenuIcon from "./icons/MenuIcon.vue";
import PopupForm from "./ui/PopupForm.vue";

export default {
  name: "navMenu",
  components: {
    LogoIcon,
    MenuIcon,
    PopupForm,
  },
  data: () => ({
    width: 0,
    scrollPosition: null,
    mobile: null,
    mobileNav: null,
  }),
  methods: {
    updateWidth() {
      this.width = window.innerWidth;
      if (this.width <= 870) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },
  },
  mounted() {
    this.updateWidth();
  },
  created() {
    window.addEventListener("resize", this.updateWidth);
  },
};
</script>
<style lang="scss">

.logo-header {
  width: 160px !important;
}

.btn-main {
  border-radius: 40px;
  background-color: $secondary !important;
  font-size: 16px;
  font-weight: 700;
  color: #fff !important;
}

.menu-item {
  font-weight: 500;
  font-size: 16px;
  color: #000 !important;
  margin-left: 40px;
}

.v-toolbar__content {
  width: 1185px;
  margin: 0 auto;
}

.container--fluid {
  padding: 0;
}

header {
  background-color: $bckg-blue;
  z-index: 99;
  width: 100%;
  position: fixed;
  transition: 0.5s ease all;

  nav {
    position: relative;
    display: flex;
    flex-direction: row;
    padding: 12px 0;
    transition: 0.5s ease all;
    width: 90%;
    margin: 0 auto;
    @media (min-width: 1185px) {
      max-width: 1185px;
    }

    ul,
    .link {
      font-weight: 500;
      color: #000;
      list-style: none;
      text-decoration: none;
    }

    .link {
      font-size: 18px;
      transition: 0.5s ease all;
      padding-bottom: 4px;
      border-bottom: 1px solid transparent;

      &:hover {
        color: $primary;
        border-color: $primary;
      }
    }

    .branding {
      display: flex;
      align-items: center;

      svg {
        width: 50px;
        transition: 0.5s ease all;
      }
    }

    .navigation {
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;

      &__list {
        display: flex;
      }
    }

    .icon {
      display: block;
      align-items: center;
      position: relative;
      top: 0;
      right: 24px;
      height: 100%;
      margin-left: 120px;
      margin-top: 5px;
      text-align: right;

      svg {
        fill: #fff;
        cursor: pointer;
        font-size: 24px;
        transition: 0.8s ease all;
      }
    }

    .icon-active {
      transition: rotate(180deg);
    }

    .dropdown-nav {
      display: flex;
      flex-direction: column;
      align-items: center;
      position: fixed;
      width: 100%;
      max-width: 250px;
      height: 100%;
      background-color: $bckg-blue;
      top: 0;
      left: 0;

      ul {
        padding: 0;
      }

      li {
        margin-top: 15px;

        a {
          margin-left: 0;
          text-align: center;
        }
      }

      button {
        background-color: $secondary !important;
        color: #fff !important;
        width: 70%;
        margin-top: 17px;
      }
    }
  }
}

.btn-main-collections {
  background-color: #58cac1 !important;
  padding: 6px 16px;
  box-shadow: 0px 3px 1px -2px rgba(0, 0, 0, 0.2), 0px 2px 2px 0px rgba(0, 0, 0, 0.14), 0px 1px 5px 0px rgba(0, 0, 0, 0.12);
}

header nav .icon {
  display: none !important;
}

header .btns-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;

  a {
    margin-right: 10px;
    min-width: 140px;
    display: block;
  }
}

@media only screen and (max-width: 600px) {
  header nav .icon {
    display: block !important;
    right: 0;
    top: -8px;
  }
  .dropdown-nav button{
    margin: 30px;
    .v-btn__content {
      padding: 20px !important;
    }
  }
}
</style>
