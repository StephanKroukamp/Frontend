<template>
  <v-container>
    <v-row>
      <v-col>
        <v-toolbar dense>
          <v-text-field
            v-model="search"
            clearable
            flat
            solo-inverted
            hide-details
            prepend-inner-icon="mdi-magnify"
            label="Search"
          >
          </v-text-field>
        </v-toolbar> 
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

export default {
  layout: "search",
  data () {
      return {
        search: ""
    }
  }
}
</script>