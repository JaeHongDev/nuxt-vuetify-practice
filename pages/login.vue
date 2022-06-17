<template>
  <v-app class="main">
  <v-container fluid pa-0>
    <v-row align="center" justify="center" style="height:100vh" dense>
      <v-col cols="12" lg="6" md="6" class="grey lighten-2 fill-height d-flex flex-column justify-center align-center">
        <v-card class ="login-wrap" flat tile>
          <v-row>
            <v-col cols="12" lg="6" md="6" class="pa-lg-10">
                <v-card-text>메시징 서비스</v-card-text>
              <consonant-selector></consonant-selector>
            </v-col>
            <v-col cols="12" lg="6" md="6">1</v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  </v-app>
</template>

<script>
export default {
  layout:'login',
  data: () => ({
    alignments: [
      'start',
      'center',
      'end',
    ],
  }),
}
</script>

<style scoped lang="scss">
.login-wrap{
  width:900px;
}

@font-face {
  font-family: 'SUIT-Medium';
  src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_suit@1.0/SUIT-Medium.woff2') format('woff2');
  font-weight: normal;
  font-style: normal;
}
.main{
  font-family: 'SUIT';
  .bold{
    font-weight: 800;
  }
  .semibold{
    font-weight: 600;
  }
}

::v-deep .v-btn {
  padding-left: 12px !important;
  padding-right: 12px !important;
}
</style>
