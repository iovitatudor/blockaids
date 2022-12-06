<template>
  <div class="text-center">
    <v-dialog v-model="dialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <v-btn class="btn-main" v-bind="attrs" v-on="on">Register</v-btn>
      </template>

      <v-card>
        <v-card-title class="text-center">
          Fill out the form to get access to our NFT collection dedicated to
          launch of new concept BlockAids Ecosystem.
        </v-card-title>

        <v-form v-model="valid" class="pop-form">
          <v-text-field
            v-model="name"
            :rules="nameRules"
            label="Name"
            required
          ></v-text-field>

          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>

          <v-text-field v-model="walletId" label="Wallet Id"></v-text-field>

          <v-text-field
            v-model="socialMedia"
            :rules="socialMediaRules"
            label="Telegram, Twitter, etc."
          ></v-text-field>
        </v-form>

        <v-card-actions>
          <PopupThanks />
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
import PopupThanks from "./PopupThanks.vue";

export default {
  components: {
    PopupThanks,
  },
};
</script>
<style lang="scss">
.pop-form {
  padding: 10px 20px;
}
</style>
