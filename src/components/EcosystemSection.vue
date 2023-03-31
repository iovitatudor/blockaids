<template>
  <v-container fluid>
    <v-container grid-list-md class="my-14">
      <p class="title-h1 text-center">Ecosystem</p>
      <v-tabs class="tab-list" centered v-model="tab">
        <v-tab key="mob-app"> Mobile App</v-tab>
        <v-tab key="tokens"> <span class="heading">Block<span>Aids </span></span> Tokens</v-tab>
        <v-tab key="dao"> <span class="heading">Block<span>Aids </span></span>  DAO</v-tab>
        <v-tab-item>
          <v-container grid-list-md>
            <v-row class="justify-center">
              <v-col lg="4" cols="11" align-self="center">
                <!--                <v-row class="align-center flex-wrap flex-lg-nowrap justify-center mt-16 mt-lg-0">-->
                <!--                  <div class="mx-4">-->
                <!--                    <p class="text-center text-lg-right mt-lg-0 mt-6">-->
                <!--                      All necessary information about services including testing and treatment.-->
                <!--                      Chatbots in a single IT system will be able to respond to low-threshold-->
                <!--                      queries related to existing needs and basic knowledge-->
                <!--                    </p>-->
                <!--                  </div>-->
                <!--                  <div class="order-first order-lg-0">-->
                <!--                    <img src="@/assets/img/ecosystem1-1.svg" alt="" />-->
                <!--                  </div>-->
                <!--                </v-row>-->
                <v-row class="align-center flex-wrap flex-lg-nowrap justify-center mt-15">
                  <div class="mx-4">
                    <p class="text-center text-lg-right w-0 mt-lg-0 mt-6">
                      Mechanisms for the protection of rights, monitoring by the community of quality and access to
                      services, the use of public resources will be strengthened
                    </p>
                  </div>
                  <div class="order-first order-lg-0">
                    <img src="@/assets/img/ecosystem1-2.png" alt=""/>
                  </div>
                </v-row>
              </v-col>
              <v-col col="11" lg="4" class="text-center order-last order-lg-0 pa-0">
                <img src="@/assets/img/unboard.png" alt=""/>
              </v-col>
              <v-col lg="4" cols="11" align-self="center">
                <v-row class="align-center flex-wrap flex-lg-nowrap justify-center mt-16 mt-lg-0">
                  <div><img src="@/assets/img/ecosystem1-3.svg" alt=""/></div>
                  <div class="mx-4">
                    <p class="text-center text-lg-left mt-lg-0 mt-6">
                      All necessary information about services including testing and treatment. Chatbots in a single IT
                      system will be able to respond to low-threshold queries related to existing needs and basic
                      knowledge
                    </p>
                  </div>
                </v-row>
                <!--                <v-row class="align-center flex-wrap flex-lg-nowrap justify-center mt-15">-->
                <!--                  <div><img src="@/assets/img/ecosystem1-4.svg" alt="" /></div>-->
                <!--                  <div class="mx-4">-->
                <!--                    <p class="text-center text-lg-left mt-lg-0 mt-6">-->
                <!--                      Mechanisms for the protection of rights, monitoring by the community of-->
                <!--                      quality and access to services, the use of public resources will be-->
                <!--                      strengthened-->
                <!--                    </p>-->
                <!--                  </div>-->
                <!--                </v-row>-->
              </v-col>
            </v-row>
          </v-container>
        </v-tab-item>
        <v-tab-item>
          <v-container grid-list-md>
            <v-row class="justify-center">
              <v-col lg="4" cols="11" align-self="center">
                <v-row class="flex-wrap justify-center justify-lg-end mt-16 mt-lg-0">
                  <div class="mx-4 mt-lg-0 mt-15">
                    <p class="text-center text-lg-right">
                      <span class="heading">Block<span>Aids</span></span> tokens are a new currency with a great utility. Our tokens will
                      stimulate the community members to undertake actions that will increase their
                      health and the health of community in general, i.e. regular testing, pills
                      taking, communication with psychologists, etc.
                    </p>
                  </div>
                  <div class="order-first">
                    <img src="@/assets/img/ecosystem1-3.svg" alt=""/>
                  </div>
                </v-row>
              </v-col>
              <v-col col="11" lg="4" class="text-center order-last order-lg-0 pa-0 mt-lg-0 mt-15">
                <img src="@/assets/img/ecosystem-2.jpg" alt=""/>
              </v-col>
              <v-col lg="4" cols="11" align-self="center">
                <v-row class="flex-wrap justify-center justify-lg-start mt-16 mt-lg-0">
                  <div class="mx-4 mt-lg-0 mt-15">
                    <p class="text-center text-lg-left">
                      We are going to release a special governance token that will allow community
                      members (token holders) to vote for the most important decisions, i.e. new
                      ways of treatment adoption, important events organization, community
                      expansion, etc.
                    </p>
                  </div>
                  <div class="order-first">
                    <img src="@/assets/img/ecosystem1-3.svg" alt=""/>
                  </div>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-tab-item>
        <v-tab-item>
          <v-container grid-list-md>
            <v-row class="justify-center">
              <v-col lg="4" cols="11" align-self="center">
                <v-row class="flex-wrap justify-center justify-lg-end mt-16 mt-lg-0">
                  <div class="mx-4 mt-lg-0 mt-15">
                    <p class="text-center text-lg-right">
                      DAOs create new ways to organize the community by providing a structure that
                      communities can take advantage of to advocacy, raise funds, and deliver
                      important services. DAOs allow for more transparency in decision making and in
                      the management of organization or movement.
                    </p>
                  </div>
                  <div class="order-first">
                    <img src="@/assets/img/ecosystem1-3.svg" alt=""/>
                  </div>
                </v-row>
              </v-col>
              <v-col col="11" lg="4" class="text-center order-last order-lg-0 pa-0 mt-lg-0 mt-15">
                <img src="@/assets/img/ecosystem-3.jpg" alt="" class="third-slide"/>
              </v-col>
              <v-col lg="4" cols="11" align-self="center">
                <v-row class="flex-wrap justify-center justify-lg-start mt-16 mt-lg-0">
                  <div class="mx-4 mt-lg-0 mt-15">
                    <p class="text-center text-lg-left">
                      Through the use of smart contracts, DAOs enable community to take ownership
                      over causes they care about, and to hold organizations accountable. Through
                      tokenization, DAOs can incentivize community members to engage in charitable
                      actions and contribute to the DAO’s mission.
                    </p>
                  </div>
                  <div class="order-first">
                    <img src="@/assets/img/ecosystem1-3.svg" alt=""/>
                  </div>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-tab-item>
      </v-tabs>
    </v-container>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    tab: undefined,
  }),
};
</script>

<style lang="scss">
@import '@/assets/main.scss';

.tab-list {
  font-size: 1.2rem !important;
}

.third-slide {
  @include rwdmax(390) {
    width: 200px;
  }
}

.v-slide-group__wrapper {
  @include rwdmax(460) {
    justify-content: center;
  }
}

.v-slide-group__content {
  @include rwdmax(460) {
    display: block;
    flex: 0;
    flex-direction: column;
    height: 10px;
  }
}

.v-tabs-slider-wrapper {
  @include rwdmax(460) {
    height: 0px !important;
    position: relative;
    contain: size;
    display: block;
  }
}

.v-slide-group__wrapper {
  @include rwdmax(460) {
    display: block;
  }
}

.v-slide-group {
  height: 85px;
  margin-bottom: 20px;
}

.v-tab {
  font-size: 18px;
  margin-top: 5px;
}
</style>
