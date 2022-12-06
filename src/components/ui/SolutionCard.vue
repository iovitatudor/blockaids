<template>
  <v-col>
    <v-card color="transparent" elevation="0" class="solution mt-4">
      <v-img :src="imgUrl" contain alt="step icon" height="150" />
      <v-card-text class="justify-center text-center">{{
        step.text
      }}</v-card-text>
    </v-card>
  </v-col>
</template>
<script>
export default {
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
<style lang=""></style>
