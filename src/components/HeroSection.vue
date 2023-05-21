<template>
  <v-container fluid>
    <v-container grid-list-md class="my-14">
      <v-row justify="space-between" align="center" class="mt-16">


        <v-col md="6" sm="12">
          <h1 class="name heading" ref="name">Block<span>Aids</span></h1>
          <p class="subtitle" ref="subtitle">
            BlockAIDS, utilizing Web 3.0 technologies, amplifies response measures to HIV/AIDS worldwide
          </p>
          <p class="subsubtitle" ref="subsubtitle">
            We are launching a first decentralized Ecosystem for people living with HIV and for key and marginalised
            populations Transparent Informational System, Digital Ecosystem app on blockchain, DAO and a decentralized research
            Ecosystem. Additionally, we are launching a NFT collection that will be distributed among early supporters
            of our project.
            <!--            We are launching a first decentralized Ecosystem for HIV infected-->
            <!--            and risk groups beneficiaries that included: Transparent-->
            <!--            Informational System, Web/Mobile app on blockchain, DAO and a-->
            <!--            decentralized research Ecosystem. Additionally, we are launching a-->
            <!--            NFT collection that will be distributed among early supporters of-->
            <!--            our project.-->
          </p>
          <div class="powered-by">
            <p class="supportedBy"><span>supported by</span> UNAIDS</p>
<!--            <b class="mt-5">  powered by</b>-->
<!--            <div class="image-corner"></div>-->
<!--            <img src="@/assets/img/UNAIDS-official-logo.png" width="90%">-->
<!--            <v-img-->
<!--              src="@/assets/img/UNAIDS-official-logo.png"-->
<!--              contain-->
<!--            ></v-img>-->
          </div>
        </v-col>
        <v-col md="5" cols="0">
          <v-img
            src="@/assets/img/HeroBanner.png"
            max-height="700"
            max-width="540"
            class="hero-img"
            v-if="width >= 960"
          >
          </v-img>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    width: 0,
  }),
  methods: {
    updateWidth() {
      this.width = window.innerWidth;
    },
  },
  watch: {
    width: {
      handler() {
        if (this.width <= 960) {
          this.$refs.name.classList.add("text-center");
          this.$refs.subtitle.classList.add("text-center");
          this.$refs.subsubtitle.classList.add("text-center");
        }
      },
      deep: true,
    },
  },
  created() {
    window.addEventListener("DOMContentLoaded", this.updateWidth);
    window.addEventListener("resize", this.updateWidth);
  },
};
</script>
<style lang="scss">
.heading {
  color: #58cac1 !important;
  margin-right: 10px;

  span {
    color: #de342f !important;
    text-transform: uppercase;
  }
}

.name {
  font-size: 100px;
  color: rgb(0, 0, 0);
  font-weight: 600;
  letter-spacing: 0.09em;
  @include rwdmax(500) {
    font-size: 50px;
  }
}

.subtitle {
  color: rgb(0, 0, 0);
  font-weight: 500;
  font-size: 30px;
  line-height: 120%;
  margin-top: 30px;
}

.subsubtitle {
  color: rgb(0, 0, 0);
  font-weight: 400;
  font-size: 18px;
  line-height: 160%;
}
.powered-by {
  position: relative;
  .image-corner {
    position: absolute;
    //background-color: #FFF;
    width: 30%;
    height: 40px;
    right: 0;
    top: 0;
    z-index: 9;
  }
}
</style>
