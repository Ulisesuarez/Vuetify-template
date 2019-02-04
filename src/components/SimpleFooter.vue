<template>
  <v-footer
  class="grey lighten-3"
  height="auto"
>
  <v-card
    class="flex grey lighten-3"
    flat
    tile
  >
    <v-card-title style="margin-left: 20vw; font-size: 12px!important; font-family: serif; color: #585858" >
     &copy;2023 Zerotype. All Rights Reserved.

      <v-spacer style="max-width: 300px"></v-spacer>
      <v-flex :class="$vuetify.breakpoint.smAndDown? 'offset-xs0':''">
      <v-btn
        v-for="icon in icons"
        :key="icon"
        class="mx-2"
        light
        icon
      >
        <v-icon size="34px">{{ icon }}</v-icon>
      </v-btn>
      </v-flex>
    </v-card-title>
  </v-card>
</v-footer>
</template>

<script>
export default {
  name: 'simple-footer',
    data: () => ({
      icons: [
        'fab fa-facebook',
        'fab fa-twitter',
        'fab fa-google-plus',
        'fab fa-linkedin',
        'fab fa-instagram'
      ]
    })
}
</script>

<style scoped>

</style>
