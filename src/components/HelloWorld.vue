<template>
  <v-container mb-4 id="home">
    <v-layout>
      <v-flex xs12 offset-sm1>
        <v-card elevation="0">
          <v-card-title primary-title>
              <h1 class="display-1 mb-0"
                  style="font-family: serif, OpenSans,sans-serif !important">This is just a place holder.</h1>
          </v-card-title>
          <v-card-text>
            <v-layout wrap row>
              <v-flex class="article" d-flex xs12 sm11 md5 offset-sm1>
                <v-layout wrap>
                <v-flex  d-flex xs12 mb-3>You can remove any link to our website from this website template, you're free to use this website template without linking back to us.
                </v-flex>
                <v-flex d-flex xs12 mb-3 >This is just a place holder, so you can see what the site would look like.
                </v-flex>
                <v-flex d-flex xs12 mb-3>You can remove any link to our website from this website template, you're free to use this website template without linking back to us. This is just a place holder, so you can see what the site would look like.
                </v-flex>
                </v-layout>
              </v-flex>

              <v-flex :class="$vuetify.breakpoint.smAndDown? 'offset-sm1 article':'article'" d-flex xs12 sm11 md5 >
                <v-layout wrap>
                  <v-flex  d-flex xs12 mb-3>You can remove any link to our website from this website template, you're free to use this website template without linking back to us.
                  </v-flex>
                  <v-flex d-flex xs12 mb-3 >This is just a place holder, so you can see what the site would look like.
                  </v-flex>
                  <v-flex d-flex xs12 mb-3>You can remove any link to our website from this website template, you're free to use this website template without linking back to us. This is just a place holder, so you can see what the site would look like.
                  </v-flex>
                </v-layout>
              </v-flex>
            </v-layout>
          </v-card-text>

          <!--<v-card-actions>
            <v-btn flat color="orange">Read more</v-btn>
            <v-btn flat color="orange">Explore</v-btn>
          </v-card-actions>-->
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    ecosystem: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/vuetifyjs/vuetify-loader'
      },
      {
        text: 'github',
        href: 'https://github.com/vuetifyjs/vuetify'
      },
      {
        text: 'awesome-vuetify',
        href: 'https://github.com/vuetifyjs/awesome-vuetify'
      }
    ],
    importantLinks: [
      {
        text: 'Documentation',
        href: 'https://vuetifyjs.com'
      },
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com'
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuetifyjs.com'
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs'
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify'
      }
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com/components/api-explorer'
      },
      {
        text: 'Select a layout',
        href: 'https://vuetifyjs.com/layout/pre-defined'
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions'
      }

    ]
  })
}
</script>

<style>
  @font-face {
    font-family: 'OpenSans';
    src: url('../assets/fonts/OpenSans-Regular.eot');
    src: url('../assets/fonts/OpenSans-Regular.woff') format('woff'), url('../assets/fonts/OpenSans-Regular.ttf') format('truetype'), url('../assets/fonts/OpenSans-Regular.svg') format('svg');
    font-weight: normal;
    font-style: normal;
  }

  .article{
    font-family: Opensans, serif;
    margin: 20px;
    font-size: 16px;
  }

</style>
