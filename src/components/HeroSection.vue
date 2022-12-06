<template>
  <v-container fluid>
    <v-container grid-list-md class="my-14">
      <v-row justify="space-between" align="center" class="mt-16">
        <v-col md="6" sm="12">
          <h1 class="name" ref="name">BlockAids</h1>
          <p class="subtitle" ref="subtitle">
            Transforming the healthcare landscape all over the world
          </p>
          <p class="subsubtitle" ref="subsubtitle">
            We are launching a first decentralized Ecosystem for HIV infected
            and risk groups beneficiaries that included: Transparent
            Informational System, Web/Mobile app on blockchain, DAO and a
            decentralized research Ecosystem. Additionally, we are launching a
            NFT collection that will be distributed among early supporters of
            our project.
          </p>
        </v-col>
        <v-col md="5" sm="0">
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
          this.$refs.logo.classList.add("logo-small");
        }
      },
      deep: true,
    },
  },
  created() {
    window.addEventListener("resize", this.updateWidth);
  },
};
</script>
<style lang="scss">
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
</style>
