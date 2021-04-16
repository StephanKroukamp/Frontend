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
        label="Artists"
      >
      </v-text-field>
    </v-toolbar>
    
    <v-card>
      <v-list rounded>
        <v-list-item 
          v-for="artist in artists"
          :key="artist.name"
        >
          <v-list-item-avatar left>
            <img
              :src="artist.coverArt"
              :alt="artist.name"
            >
          </v-list-item-avatar>

          <v-list-item-title v-text="artist.name"/>
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
        artists: [
          { "id": 1, "name": "Camel Power Club", "coverArt": "https://picsum.photos/id/1/200/300" },
          { "id": 2, "name": "Mind Against", "coverArt": "https://picsum.photos/id/2/200/300" },
          { "id": 3, "name": "Tale Of Us", "coverArt": "https://picsum.photos/id/3/200/300" },
          { "id": 4, "name": "Lamb Of God", "coverArt": "https://picsum.photos/id/4/200/300" },
          { "id": 5, "name": "Bring Me The Horizon", "coverArt": "https://picsum.photos/id/5/200/300" },
          { "id": 6, "name": "Architects", "coverArt": "https://picsum.photos/id/6/200/300" },
          { "id": 7, "name": "Parkway Drive", "coverArt": "https://picsum.photos/id/7/200/300" },
          { "id": 8, "name": "Pink Floyd", "coverArt": "https://picsum.photos/id/8/200/300" },
          { "id": 9, "name": "Kygo", "coverArt": "https://picsum.photos/id/9/200/300" },
          { "id": 10, "name": "Ry X", "coverArt": "https://picsum.photos/id/10/200/300" },
          { "id": 11, "name": "Rise Against", "coverArt": "https://picsum.photos/id/11/200/300" },
          { "id": 12, "name": "Gojira", "coverArt": "https://picsum.photos/id/12/200/300" },
          { "id": 13, "name": "Gryffin", "coverArt": "https://picsum.photos/id/13/200/300" },
          { "id": 14, "name": "Dire Straits", "coverArt": "https://picsum.photos/id/14/200/300" },
          { "id": 15, "name": "The Police", "coverArt": "https://picsum.photos/id/15/200/300" },
          { "id": 16, "name": "Boston", "coverArt": "https://picsum.photos/id/16/200/300" },
          { "id": 17, "name": "Denis Horvat", "coverArt": "https://picsum.photos/id/17/200/300" },
          { "id": 18, "name": "ZHU", "coverArt": "https://picsum.photos/id/18/200/300" },
          { "id": 19, "name": "Odesza", "coverArt": "https://picsum.photos/id/19/200/300" },
          { "id": 20, "name": "Adriatique", "coverArt": "https://picsum.photos/id/20/200/300" },
          { "id": 21, "name": "Stephan Bodzin", "coverArt": "https://picsum.photos/id/21/200/300" },
          { "id": 22, "name": "Killswitch Engage", "coverArt": "https://picsum.photos/id/22/200/300" },
          { "id": 23, "name": "Sylosis", "coverArt": "https://picsum.photos/id/23/200/300" },
          { "id": 24, "name": "The Blue Stones", "coverArt": "https://picsum.photos/id/24/200/300" },
          { "id": 25, "name": "Flatbush Zombies", "coverArt": "https://picsum.photos/id/25/200/300" },
          { "id": 26, "name": "Monolink", "coverArt": "https://picsum.photos/id/26/200/300" },
          { "id": 27, "name": "Kerala Dust", "coverArt": "https://picsum.photos/id/27/200/300" },
          { "id": 28, "name": "Darkside", "coverArt": "https://picsum.photos/id/28/200/300" },
          { "id": 29, "name": "Ben Bohmer", "coverArt": "https://picsum.photos/id/29/200/300" },
          { "id": 30, "name": "Boris Brejcha", "coverArt": "https://picsum.photos/id/30/200/300" }
        ]
      }
    }
  }
</script>