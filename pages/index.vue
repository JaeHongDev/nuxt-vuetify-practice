<template>
  <div>
    <Accessbility/>
    <display-breakpoint></display-breakpoint>
    <v-dialog :fullscreen="$vuetify.breakpoint.mobile">
      111
    </v-dialog>
  </div>

</template>

<script>
export default {
  name: 'IndexPage',
  data: () => ({ isMobile: false }),

  beforeDestroy () {
    if (typeof window === 'undefined') return

    window.removeEventListener('resize', this.onResize, { passive: true })
  },

  mounted () {
    this.onResize()

    window.addEventListener('resize', this.onResize, { passive: true })
  },

  methods: {
    onResize () {
      this.isMobile = window.innerWidth < 600
    },
  },
}
</script>
