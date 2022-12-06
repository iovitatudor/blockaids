<template>
  <v-row
    justify="space-between"
    align="center"
    ref="row"
    :class="[this.item.flex == 1 ? flexRow : '', 'mt-16 d-flex']"
  >
    <v-col md="6" sm="12">
      <v-img :src="imgUrl" max-height="400" max-width="400"> </v-img>
    </v-col>
    <v-col md="6" sm="12">
      <p class="mission-text">{{ item.text }}</p>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    flexRow: "flex-row-reverse",
  }),
  props: {
    item: { type: Object, required: true },
  },
  computed: {
    imgUrl() {
      return require(`@/assets/img/${this.item.img}`);
    },
  },
};
</script>
<style lang="scss">
.mission-text {
  font-weight: 400;
  font-size: 18px;
  line-height: 160%;
}

.flex-reverse {
  flex-direction: row-reverse !important;
}
</style>
