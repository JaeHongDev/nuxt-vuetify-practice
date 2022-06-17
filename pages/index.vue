<template>
  <div>
    <v-alert border="top"
             color="red lighten-2"> alert </v-alert>
    <v-alert
      border="left"
      colored-border
      color="deep-purple accent-4"
      elevation="2"
    >
      Aliquam eu nunc. Fusce commodo aliquam arcu. In consectetuer turpis ut velit. Nulla facilisi..
      Morbi mollis tellus ac sapien. Fusce vel dui. Praesent ut ligula non mi varius sagittis. Vivamus consectetuer hendrerit lacus. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
    </v-alert>
    <v-alert
      dense
      type="info"
    >
      I'm a dense alert with a <strong>type</strong> of info
    </v-alert>

    <v-alert
      v-model="alert"
      border="left"
      close-text="Close Alert"
      color="deep-purple accent-4"
      dark
      dismissible
    >
      Aenean imperdiet. Quisque id odio. Cras dapibus. Pellentesque ut neque. Cras dapibus.

      Vivamus consectetuer hendrerit lacus. Sed mollis, eros et ultrices tempus, mauris ipsum aliquam libero, non adipiscing dolor urna a orci. Sed mollis, eros et ultrices tempus, mauris ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur blandit mollis lacus. Curabitur ligula sapien, tincidunt non, euismod vitae, posuere imperdiet, leo.
    </v-alert>
    <div class="text-center">
      <v-btn
        v-if="!alert"
        @click="alert = true"
      >
        Reset
      </v-btn>
    </div>
    <v-alert
      color="#2A3B4D"
      icon="mdi-firework"
    >
      Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi. Vivamus quis mi. Quisque ut nisi. Maecenas malesuada.
    </v-alert>
    <v-alert
      color="primary"
      icon="mdi-vuetify"
      border="left"
      prominent
    >
      Praesent congue erat at massa. Nullam vel sem. Aliquam lorem ante, dapibus in, viverra quis, feugiat a, tellus. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. Curabitur at lacus ac velit ornare lobortis.
    </v-alert>

    <v-alert
      prominent
      type="error"
    >
      <v-row align="center">
        <v-col class="grow">
          Nunc nonummy metus. Nunc interdum lacus sit amet orci. Nullam dictum felis eu pede mollis pretium. Cras id dui.
        </v-col>
        <v-col class="shrink">
          <v-btn>Take action</v-btn>
        </v-col>
      </v-row>
    </v-alert>

    <v-card class="t">1111</v-card>

    <v-container>
      <v-row justify="center">
        <v-col cols="6">
          <v-card class="black fs-1" >
            <v-card-title class="green darken-4 fs-1">Chocolate cheesecake recipe</v-card-title>
            <v-card-text class="pt-2">
              <ul class="subtitle-2">
                <li>5 eggs</li>
                <li>1 cup of warm milk</li>
                <li>2 cups of flour</li>
                <li>1/2 cup of sugar</li>
                <li class="red--text">1 lbs Philadelphia cream cheese </li>
                <li>...</li>
              </ul>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <v-card class="xidps-card" color="yellow">
      <v-col cols="6" class="yellow">
        <div class="fill-height d-flex justify-center align-center">this should be different color</div>
      </v-col>
      <v-col cols="6" class="yellow">
        <div class="fill-height d-flex justify-center align-center">this should be different color</div>
      </v-col>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      alert: true,
      rules: [
        value => !!value || 'Required.',
        value => (value && value.length >= 3) || 'Min 3 characters',
      ],
    }
  },
}
</script>

<style lang="scss">
.xidps-card{
  ::v-deep{
    background-color: #efefef;
  }
}
</style>
