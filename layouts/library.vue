<template>
  <v-app id="musicStore">
    <v-main>
      <v-container
        fluid
      >
        <v-row>
          <v-col>
            <v-tabs
              v-model="tab"
              centered
              icons-and-text
              exact
              nuxt
            >
              <v-tabs-slider></v-tabs-slider>

              <v-tab
                v-for="tab in tabs"
                :key="tab.title"
                :to="tab.to"
              >
                {{tab.title}}
                <v-icon>{{tab.icon}}</v-icon>
              </v-tab>
            </v-tabs>
          </v-col>
        </v-row>

        <v-row>
          <v-col>
            <nuxt/>
          </v-col>
        </v-row>

        <v-row>
          <v-col>
            <v-bottom-navigation fixed>
              <v-btn
                v-for="bottomNavigationButton in bottomNavigationButtons"
                :key="bottomNavigationButton.title"
                :to=bottomNavigationButton.to
                exact
              >
                <span>{{bottomNavigationButton.title}}</span>

                <v-icon>{{bottomNavigationButton.icon}}</v-icon>
              </v-btn>
            </v-bottom-navigation>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        bottomNavigationButtons: [
          {
            title: "Home",
            to: "/",
            icon: "mdi-home"
          },
          {
            title: "Search",
            to: "/search",
            icon: "mdi-magnify"
          },
          {
            title: "Library",
            to: "/library/playlists",
            icon: "mdi-book-open-page-variant"
          }
        ],
        tab: null,
        tabs: [
          {
            title: "Playlists",
            to: "/library/playlists",
            icon: "mdi-playlist-music-outline"
          },
          {
            title: "Artists",
            to: "/library/artists",
            icon: "mdi-account-music"
          },
          {
            title: "Albums",
            to: "/library/albums",
            icon: "mdi-album "
          }
        ]
      }
    }
  }
</script>