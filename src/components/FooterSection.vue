<template>
  <v-container class="bckg footer" fluid>
    <v-container grid-list-md class="my-14">
      <v-row justify="space-between">
        <v-col align="center" cols="2">
          <LogoIcon />
          <v-row justify="center" align="center" class="mt-5">
            <a
              class="mx-2"
              target="_blank"
              href="https://ro-ro.facebook.com/initiativapozitiva/"
              ><FbIcon
            /></a>
            <a
              class="mx-2"
              target="_blank"
              href="https://www.instagram.com/positivepeople.md/"
              ><InstIcon
            /></a>
            <a
              class="mx-2"
              target="_blank"
              href="https://www.youtube.com/c/InitiativaPozitiva"
              ><YtIcon /> </a
          ></v-row>
        </v-col>
        <v-col align-self="center" md="6">
          <v-row>
            <v-col md="4">
              <ul>
                <li class="footer__text"><b>About</b></li>
                <li class="footer__text">
                  <a class="footer__link" href="">Business model</a>
                </li>
                <li class="footer__text">
                  <a class="footer__link" href="">Team</a>
                </li>
              </ul>
            </v-col>
            <v-col md="3">
              <ul>
                <li class="footer__text"><b>Roadmap</b></li>
                <li class="footer__text">
                  <a class="footer__link" href="">Pitchdeck </a>
                </li>
              </ul>
            </v-col>
            <v-col md="5">
              <ul>
                <li class="footer__text"><b>Keep in touch</b></li>
                <li class="footer__text">
                  <a class="footer__link" href="mailto:aidsblock@gmail.com"
                    ><b>Mail</b>:: aidsblock@gmail.com</a
                  >
                </li>
              </ul>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>
<script>
import LogoIcon from "./icons/LogoIcon.vue";
import FbIcon from "./icons/FbIcon.vue";
import InstIcon from "./icons/InstIcon.vue";
import YtIcon from "./icons/YtIcon.vue";

export default { components: { LogoIcon, FbIcon, InstIcon, YtIcon } };
</script>
<style lang="scss">
.footer {
  &__text {
    color: #000;
  }
  a {
    color: #000 !important;
  }
}
</style>
