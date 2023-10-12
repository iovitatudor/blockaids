<template>
  <v-container fluid id="team">
    <v-container grid-list-md class="my-14">
      <h1 class="title-h1 text-center mb-5">Our Team</h1>
      <v-row justify="center" align="center" class="mt-16">
        <TeamCard
          v-for="(member, index) in members"
          :key="index"
          :member="member"
        />
      </v-row>
    </v-container>
  </v-container>
</template>
<script>
import TeamCard from "./ui/TeamCard.vue";

export default {
  components: {
    TeamCard,
  },
  data: () => ({
    members: [
      {
        id: 0,
        photo: "team1.jpg",
        name: "Constantin Cearanovski",
        role: "CEO Digital Public Health consortium",
      },
      {
        id: 1,
        photo: "team2.jpg",
        name: "Ruslan Poverga",
        role: "Co-Founder and CEO – NGO Positive Initiative",
      },
      {
        id: 2,
        photo: "team3.png",
        name: "Andrei Tintari",
        role: "Web3 Moldova Community Founder, CTO",
      },
      {
        id: 3,
        photo: "image-Max-591.png",
        name: "Maxim Demchenko",
        role: "Public health domain expert",
      },
      {
        id: 4,
        photo: "alexandra-image.png",
        name: "Alexandra Volgina",
        role: "Human rights protection and advocacy expert",
      },
      {
        id: 5,
        photo: "Dmitriev Sergii CEO Health Advocacy Coalition 640.jpg",
        name: "Dmitriev Sergii",
        role: "CEO Health Advocacy Coalition",
      },
      {
        id: 7,
        photo: "Anna-image-640.png",
        name: "Anna Koshikova",
        role: "CEO Eurasian movement for the RIGHT TO HEALTH IN PRISONS",
      },
      {
        id: 6,
        photo: "Giorgi Soselia CEO Social Equation Hub 640.jpg",
        name: "Giorgi Soselia",
        role: "CEO Social Equation Hub",
      },
      {
        id: 7,
        photo: "miguel.jpg",
        name: "Miguel Francis-Santiago",
        role: "Global Digital ID Lead, Web3 PR Executive",
      },
    ],
  }),
};
</script>
<style lang=""></style>
