<template>
  <v-container fluid id="solution">
    <v-container grid-list-md class="my-14">
      <p class="title-h1 text-center">Our Solution</p>
      <p class="subsubtitle text-center">
        A transformative, highly secure, and self-sustaining healthcare
        ecosystem secured by Blockchain.
      </p>
      <v-row>
        <SolutionCard
          v-for="(step, index) in steps"
          :key="index"
          :step="step"
        />
      </v-row>
    </v-container>
  </v-container>
</template>
<script>
import SolutionCard from "@/components/ui/SolutionCard.vue";

export default {
  components: {
    SolutionCard,
  },

  data: () => ({
    steps: [
      {
        icon: "solution_icon1.svg",
        text: "BlockAIDS cultivates a global community in the field of HIV/AIDS, uniting interested people around shared goals and values. This implies the use of Web 3.0 technologies for a decentralized (DAO) governance structure, equal participation, and decision-making.",
      },
      {
        icon: "solution_icon2.svg",
        text: "BlockAIDS prioritizes the promotion of equality, including gender and racial equality, equal rights in access to healthcare services, absence of any forms of discrimination. Using Web 3.0 technologies, communities can advocate for their values and rights, striving for access to vital medical services and support.",
      },
      {
        icon: "solution_icon3.svg",
        text: "BlockAIDS shifts the paradigm of fundraising and funds’ distribution, creating a more transparent and decentralized model that allows communities to access resources needed for implementing priorities. This will help eliminate longstanding inequality in funding distribution, prioritizing resources based on the real needs of communities, rather than politics, power, or influence.",
      },
      {
        icon: "solution_icon4.svg",
        text: "BlockAIDS aims to expand access to medical and social services, especially in regions with limited access. By utilizing Web 3.0 technologies, decentralized platforms will allow people to access medical care from any location worldwide, enhancing accessibility, reducing barriers to assistance, and increasing control over their own data.",
      },
    ],
  }),
};
</script>
<style lang=""></style>
