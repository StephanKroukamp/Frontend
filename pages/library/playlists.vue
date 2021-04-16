<template>
  <div>
    <v-toolbar>
      <v-text-field
        v-model="search"
        clearable
        flat
        solo-inverted
        hide-details
        prepend-inner-icon="mdi-magnify"
        label="Playlists"
      >
      </v-text-field>
    </v-toolbar>
    
    <v-card>
      <v-list rounded>
        <v-list-item 
          v-for="playlist in playlists"
          :key="playlist.name"
        >
          <v-list-item-avatar left>
            <img
              :src="playlist.coverArt"
              :alt="playlist.name"
            >
          </v-list-item-avatar>

          <v-list-item-title v-text="playlist.name"/>
        </v-list-item>
      </v-list>
    </v-card>
  </div>
</template>

<script>
  export default {
    layout: "library",
    data () {
      return {
        search: "",
        playlists: [
          { "id": 1, "name": "Favourites", "coverArt": "https://picsum.photos/id/1/200/300" },
          { "id": 2, "name": "Deep Techno", "coverArt": "https://picsum.photos/id/2/200/300" },
          { "id": 3, "name": "Funky", "coverArt": "https://picsum.photos/id/3/200/300" },
          { "id": 4, "name": "Breakdown Central", "coverArt": "https://picsum.photos/id/4/200/300" },
          { "id": 5, "name": "Invigorous", "coverArt": "https://picsum.photos/id/5/200/300" },
          { "id": 6, "name": "Uplifting", "coverArt": "https://picsum.photos/id/6/200/300" },
          { "id": 7, "name": "Timeless Classics", "coverArt": "https://picsum.photos/id/7/200/300" },
          { "id": 8, "name": "Guilty Pleasure", "coverArt": "https://picsum.photos/id/8/200/300" },
          { "id": 9, "name": "Pumped", "coverArt": "https://picsum.photos/id/9/200/300" },
          { "id": 10, "name": "Chill", "coverArt": "https://picsum.photos/id/10/200/300" }
        ]
      }
    }
  }
</script>