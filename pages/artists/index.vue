<template>
  <v-container>
    <v-row dense>
      <v-col>
        <v-app-bar color="accent">
          <v-toolbar-title>Artists</v-toolbar-title>

          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
        </v-app-bar>
      </v-col>
    </v-row>

    <br>

    <v-container class="grey lighten-5">
      <v-row>
        <v-col
          v-for="(artist, i) in artists" 
          :key="i"
          sm="12"
          md="6"
          lg="4"
          xl="3"
        >
          <v-card
            :color="randomizeColor()"
            dark
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="text-h5 artist-name"
                  v-text="artist.name"
                ></v-card-title>

                <v-card-subtitle v-for="(track, i) in artist.tracks" :key="i" >
                  {{track.name}}
                </v-card-subtitle>

                <v-card-actions>
                  <v-btn
                    class="ml-2 mt-3"
                    fab
                    icon
                    height="40px"
                    right
                    width="40px"
                  >
                    <v-icon>mdi-play</v-icon>
                  </v-btn>
                </v-card-actions>
              </div>
              
              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="artist.coverArt"></v-img>
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>

export default {
  name:"index",
  async asyncData({ $axios }) {
    const artists = await $axios.$get('/artists')

    return { artists }
  },
  methods: {
    randomizeColor: function () {
      const colors = ['#F44336', '#2196F3', '#009688'];

      const random = Math.floor(Math.random() * colors.length);

      return colors[random]
    }
  }
}
</script>

<style scoped>
  .artist-name {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
</style>