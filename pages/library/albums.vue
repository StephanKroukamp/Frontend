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
        label="Albums"
      >
      </v-text-field>
    </v-toolbar>
    
    <v-card>
      <v-list rounded>
        <v-list-item 
          v-for="album in albums"
          :key="album.name"
        >
          <v-list-item-avatar left>
            <img
              :src="album.coverArt"
              :alt="album.name"
            >
          </v-list-item-avatar>

          <v-list-item-title v-text="album.name"/>
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
        albums: [
          { "id": 1, "name": "Fear Inocolum", "coverArt": "https://picsum.photos/id/1/200/300" },
          { "id": 2, "name": "Oposites", "coverArt": "https://picsum.photos/id/2/200/300" },
          { "id": 3, "name": "That's The Spirit", "coverArt": "https://picsum.photos/id/3/200/300" },
          { "id": 4, "name": "Rocco", "coverArt": "https://picsum.photos/id/4/200/300" },
          { "id": 5, "name": "Amniotic", "coverArt": "https://picsum.photos/id/5/200/300" },
          { "id": 6, "name": "Golden Hour", "coverArt": "https://picsum.photos/id/6/200/300" },
          { "id": 7, "name": "Dormant Heart", "coverArt": "https://picsum.photos/id/7/200/300" }
        ]
      }
    }
  }
</script>