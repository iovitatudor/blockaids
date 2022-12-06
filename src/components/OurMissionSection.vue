<template>
  <v-container fluid class="bckg">
    <v-container grid-list-md class="my-14">
      <p class="title-h1 text-center">Our Mission</p>

      <MissionCard v-for="(item, index) in items" :key="index" :item="item" />
    </v-container>
  </v-container>
</template>
<script>
import MissionCard from "./ui/MissionCard.vue";

export default {
  components: {
    MissionCard,
  },

  data: () => ({
    items: [
      {
        img: "Mission1.png",
        text: "To increase availability, quality and suitability of services, for HIV treatment, testing and prevention, so that everyone is well-served.To reform laws, policies and practices to tackle the stigma and exclusion faced by people living with HIV and by key and marginalised populations, so that everyone is shown respect and is welcomed.",
        flex: 0,
      },
      {
        img: "Mission2.png",
        text: "To ensure the sharing of technology to enable equal access to the best HIV science, between communities and between the Global South and North.To promote interoperability of all elements of the health data ecosystem through a common ontology and data standards.",
        flex: 1,
      },
      {
        img: "Mission3.png",
        text: "To empowere people through increased digital access and control over personal electronic health data.To develop an intersectoral partnership to consolidate a common vision and priorities in the field of transformation of public health systems.To provide open access to strategic data to improve global health.",
        flex: 0,
      },
    ],
  }),
};
</script>
<style lang="scss">
.title-h1 {
  font-weight: 700 !important;
  font-size: 48px !important;
}

.bckg {
  background-color: $bckg-blue;
}
</style>
