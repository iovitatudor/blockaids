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
        <RoadmapCard v-for="(step, index) in steps" :key="index" :step="step"/>
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
        date: "2023",
        text: [
          "- Development of Mobile App (Moldova) integrated with Web3",
          "- Creating DAO for people living with HIV & key affected populations",
        ],
      },
      {
        date: "2024",
        text: [
          "- Digitalization (Mobile App on the blockchain in EECA countries)",
          "- Expanding DAO in EECA countries",
        ],
      },
      {
        date: "2025",
        text: [
          "- Digitalization (Mobile App on the blockchain in Africa countries)",
          "- Expanding DAO in Africa countries"
        ],
      },
      {
        date: "2026",
        text: [
          "- Digitalization (Mobile App on the blockchain in rest of the world countries)",
          "- Expanding DAO in rest of the world countries",
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
