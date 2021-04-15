<template>
  <v-app id="musicStore">
    <v-app-bar app color="primary">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-btn icon to="/">
        <v-icon>mdi-home</v-icon>
      </v-btn>

      <v-toolbar-title v-text="title"></v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <v-list>
        <v-list-item router exact to="/artists">
          <v-list-item-content>
            <v-list-item-title>Artists</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item router exact to="/tracks">
          <v-list-item-content>
            <v-list-item-title>Tracks</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item router exact to="/albums">
          <v-list-item-content>
            <v-list-item-title>Albums</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  
    <v-main>
      <nuxt/>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      title: "Music Store",
      drawer: null
    })
  }
</script>