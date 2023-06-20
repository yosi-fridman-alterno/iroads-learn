<template>
  <!-- <v-parallax src="@/assets/background.png" /> -->

  <div class="backgroundImage">

    <v-container class="text-center padding-bottom-medium ">
      <v-row justify="center" class="dirRTL alignCenter">
        <v-col cols="12" sm="6" md="2">
          <v-btn block rounded="xl" size="x-large" @click="onClickTile1" class="roundedButton">פורטל ארגוני</v-btn>
        </v-col>

        <v-col cols="12" sm="6" md="2">
          <v-btn block rounded="xl" size="x-large" @click="onClickTile2" :disabled="disableTile2" class="roundedButton">
            ניהול מסמכים
          </v-btn>
        </v-col>

        <v-col cols="12" sm="6" md="2">
          <v-btn block rounded="xl" size="x-large" @click="onClickTile3" :disabled="disableTile3"
            class="roundedButton">חילן</v-btn>
        </v-col>

        <v-col cols="12" sm="6" md="2">
          <v-btn block rounded="xl" size="x-large" @click="onClickTile4" :disabled="disableTile4"
            class="roundedButton">זימונתי</v-btn>
        </v-col>

        <v-col cols="12" sm="6" md="2">
          <v-btn block rounded="xl" size="x-large" @click="onClickTile5" :disabled="disableTile5"
            class="roundedButton">המערכות שלנו</v-btn>
        </v-col>

        <v-col cols="12" sm="6" md="2">
          <v-btn block rounded="xl" size="x-large" @click="onClickTile6" :disabled="disableTile6"
            class="roundedButton">יישומים</v-btn>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>

export default {

  data() {
    return {
      disableTile2: true,
      disableTile3: true,
      disableTile4: true,
      disableTile5: true,
      disableTile6: true
    }
  },

  methods: {
    onClickTile1() {
      this.disableTile2 = false;
      window.open("http://www.iroads.co.il", "_blank")
    },
    onClickTile2() {
      this.disableTile3 = false;
      window.open("http://www.google.co.il", "_blank")
    },
    onClickTile3() {
      this.disableTile4 = false;
      window.open("http://www.ynet.co.il", "_blank")
    },
    onClickTile4() {
      this.disableTile5 = false;
      window.open("http://www.n12.co.il", "_blank")
    },
    onClickTile5() {
      this.disableTile6 = false;
      window.open("http://www.walla.co.il", "_blank")
    },
    onClickTile6() {
      this.disableTile6 = false;
      window.open("http://www.bing.com", "_blank")
    }
  }


}

</script>

<style scoped>
.backgroundImage {

  background-image: url("@/assets/background.png");
  background-color: #cccccc;
  background-size: contain;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}

.roundedButton {

  width: 10rem;
  height: 10rem;
  min-width: 10rem;
  max-width: 10rem;
  min-height: 10rem;
  max-height: 10rem;
  border-radius: 5rem !important;

}

.padding-bottom-medium {
  padding-bottom: 1rem;
}

.dirRTL {
  direction: rtl;
}



.alignCenter {
  text-align: -webkit-center
}
</style>

