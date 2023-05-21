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
          "- Establishing a Decentralized Autonomous Organization (DAO) to empower people living with HIV and key affected populations, promoting equal participation and decision-making in the Eastern Europe and Central Asia (EECA) region.",
          "- Leveraging blockchain technology to ensure equal rights to healthcare services, eliminate all forms of discrimination, and enhance security and transparency. This improves access to medical and social services in the EECA region.",
        ],
      },
      {
        date: "2024",
        text: [
          "- Expanding the DAO to include African countries.",
          "- Expanding blockchain technology solutions in African countries.",
        ],
      },
      {
        date: "2025",
        text: [
          "- Expanding the DAO to cover the rest of the world.",
          "- Expanding blockchain technology solutions to countries across the globe."
        ],
      },
      // {
      //   date: "2026",
      //   text: [
      //     "- Digitalization (Mobile App on the blockchain in rest of the world countries)",
      //     "- Expanding DAO in rest of the world countries",
      //   ],
      // },
    ],
  }),
  created() {
    window.addEventListener("resize", this.updateWidth);
  },
};
</script>
<style lang=""></style>
