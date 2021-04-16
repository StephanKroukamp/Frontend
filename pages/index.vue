<template>
  <div>
      <v-row>
        <v-col>
            <v-card>
                <v-card-title class="headline">
                    Unlimited music now
                </v-card-title>

                <v-card-subtitle>Listen to your favorite artists and albums whenever and wherever, online and offline.</v-card-subtitle>

                <v-card-actions>
                <v-btn
                    text
                    to="/search">
                    Listen Now
                </v-btn>
                </v-card-actions>
            </v-card>
        </v-col>
    </v-row>

    <v-row>
        <v-col>
            <v-parallax
                src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
            >
                <v-row
                    align="center"
                    justify="center"
                >
                    <v-col
                        class="text-center"
                        cols="12"
                    >
                        <h1 class="display-1 font-weight-thin mb-4">
                            Stephan's Spotify Clone
                        </h1>
                        
                        <h4 class="subheading">
                            Still need to make it my own ;)
                        </h4>
                    </v-col>
                </v-row>
            </v-parallax>
        </v-col>
    </v-row>
  </div>
</template>

<script>

export default {
    layout: 'home'
}
</script>