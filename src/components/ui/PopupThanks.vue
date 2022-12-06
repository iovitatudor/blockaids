<template>
  <v-dialog v-model="thanks" width="500">
    <template v-slot:activator="{ on, attrs }">
      <v-btn class="btn-main mx-auto" v-bind="attrs" v-on="on">Register</v-btn>
    </template>

    <v-card>
      <v-card-title class="text-center pa-10">
        Thank You! We will contact You soon!
      </v-card-title>
    </v-card>
  </v-dialog>
</template>
<script>
export default {};
</script>
<style lang=""></style>
