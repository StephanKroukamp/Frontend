<template>
  <div>
    <v-card
      v-for="(category, i) in categories" 
      :key="i"
    >
      <v-card-title
      >
        {{category.title}}
      </v-card-title>
    </v-card>
  </div>
</template>

<script>

export default {
  layout: "search",
  data () {
      return {
        categories: [
          {
            title: "Rock",
          },
          {
            title: "Dance/Electronic"
          },
          {
            title: "Metal"
          },
          {
            title: "Pop"
          },
          {
            title: "Hip Hop"
          },
          {
            title: "Country"
          },
          {
            title: "Soul"
          },
          {
            title: "Techno"
          }
        ]
      }
    }
}
</script>