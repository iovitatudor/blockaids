<template>
  <v-container fluid>
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
        text: "The information system through mobile APP will provide online access to medical and social services for key groups and PLHIV on the basis of a one-stop shop for community-based organizations, as well as organizations of state medical structures.",
      },
      {
        icon: "solution_icon2.svg",
        text: "Unique token-reward technology incentivising behaviour change in patients and healthcare workers for improved health and well-being",
      },
      {
        icon: "solution_icon3.svg",
        text: "A DAO for each community (AIDS, LGBT, Sexual workers, drug users) that allows members to participate equally in important decisions voting",
      },
      {
        icon: "solution_icon4.svg",
        text: "Decentralized ecosystem will provide the community with all necessary learning and communication resources, i.e. web pages with information, social networks for communication, learn2earn, events and NFT rewards.",
      },
    ],
  }),
};
</script>
<style lang=""></style>
