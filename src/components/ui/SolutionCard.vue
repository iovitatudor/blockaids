<template>
  <v-col cols="12" md="3">
    <v-card color="transparent" elevation="0" class="solution mt-4">
      <v-img :src="imgUrl" contain alt="step icon" height="100" />
      <v-card-text class="solution-text justify-center text-left">{{
        step.text
      }}</v-card-text>
    </v-card>
  </v-col>
</template>
<script>
export default {
  name: "SolutionCard",
  props: {
    step: { type: Object, required: true },
  },
  computed: {
    imgUrl() {
      return require(`@/assets/img/${this.step.icon}`);
    },
  },
};
</script>
<style lang="scss">
.solution-text {
  font-weight: 400;
  font-size: 18px;
  line-height: 160%;
}
</style>
