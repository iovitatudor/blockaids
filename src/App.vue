<template>
  <v-app>
    <NavBar />
    <HeroSection />
    <SolutionSection />
    <EcosystemSection />
    <OurMissionSection />
    <PartnersSection />
    <TeamSection />
    <RoadmapSection />
    <FooterSection />
  </v-app>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import HeroSection from "@/components/HeroSection.vue";
import OurMissionSection from "./components/OurMissionSection.vue";
import SolutionSection from "./components/SolutionSection.vue";
import EcosystemSection from "./components/EcosystemSection.vue";
import PartnersSection from "./components/PartnersSection.vue";
import TeamSection from "./components/TeamSection.vue";
import RoadmapSection from "./components/RoadmapSection.vue";
import FooterSection from "./components/FooterSection.vue";

export default {
  name: "App",

  components: {
    NavBar,
    HeroSection,
    OurMissionSection,
    SolutionSection,
    PartnersSection,
    TeamSection,
    RoadmapSection,
    FooterSection,
    EcosystemSection,
  },

  data: () => ({
    //
  }),
};
</script>
