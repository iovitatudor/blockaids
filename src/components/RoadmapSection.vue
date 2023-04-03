<template>
  <v-container fluid id="roadmap">
    <v-container grid-list-md class="my-14">
      <h1 class="title-h1 text-center mb-5">Roadmap</h1>
      <v-img
        src="@/assets/img/roadmap.svg"
        contain
        height="150"
        v-if="width >= 960"
      ></v-img>

      <v-row class="mt-7">
        <RoadmapCard v-for="(step, index) in steps" :key="index" :step="step" />
      </v-row>
    </v-container>
  </v-container>
</template>
<script>
import RoadmapCard from "./ui/RoadmapCard.vue";

export default {
  components: {
    RoadmapCard,
  },
  methods: {
    updateWidth() {
      this.width = window.innerWidth;
    },
  },
  data: () => ({
    width: 0,
    steps: [
      {
        date: "2022",
        text: [
          "- Building community of people living with HIV and  groups of risk in Moldova (more than 30k membars)",
        ],
      },
      {
        date: "2023",
        text: [
          "- Creating DAO for communities",
          "- Creating DAOs for small communities (i.e. groups of risk)",
          "- Governance token release",
        ],
      },
      {
        date: "2023",
        text: [
          "Building Web/Mobile app on blockchain:",
          "- Identification (KYC)",
          "- Transparency",
          "- Anonymity",
          "- Unified information and tracking system",
        ],
      },
      {
        date: "2024",
        text: [
          "Building new ecosystem of people living with HIV and  groups of risk:",
          "- Anonymous social groups",
          "- Learning resources, incl. Learn2Earn",
          "- Events organization",
          "- NFT/token rewards programs",
        ],
      },
    ],
  }),
  created() {
    window.addEventListener("resize", this.updateWidth);
  },
};
</script>
<style lang=""></style>
