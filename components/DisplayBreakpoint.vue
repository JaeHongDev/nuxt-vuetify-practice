<!-- Vue Component -->

<template>
  <v-card :height="height">
      aaaa
  </v-card>
</template>

<script>
export default {
  computed: {
    height () {
      console.log(1);
      switch (this.$vuetify.breakpoint.name) {
        case 'xs': return 220
        case 'sm': return 400
        case 'md': return 500
        case 'lg': return 600
        case 'xl': return 800
      }
    },
  },
}
</script>
