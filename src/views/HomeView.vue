<template>
  <v-container>
    <v-card class="mx-auto" max-width="700">
      <v-card-text>
        <v-row align="center" no-gutters>
          <v-col class="text-left">
            <v-avatar color="grey" class="w-sm-25 h-sm-25 h-50 w-50">
              <v-img src="https://avatars.githubusercontent.com/u/85351652?v=4" />
            </v-avatar>
          </v-col>
          <v-col class="d-flex flex-column ga-3">
            <v-card-title class="px-0">reiyuchan</v-card-title>
            <p><v-icon>mdi mdi-music</v-icon> Hobbyist Music Producer</p>
            <p><v-icon>mdi mdi-heart</v-icon> Gaming, Linux, Music</p>
            <p><v-icon>mdi mdi-code-braces</v-icon> JavaScript/TypeScript, Java, PHP, C#, Go</p>
          </v-col>
        </v-row>
      </v-card-text>
      <v-spacer />
      <v-card-actions class="d-flex ga-4">
        <v-btn href="mailto:iwakura.rei.tk@gmail.com" icon><v-icon>fas fa-envelope</v-icon></v-btn>
        <v-btn href="https://github.com/reiyuchan" target="_blank" icon><v-icon>fab fa-github</v-icon></v-btn>
        <v-btn href="https://keybase.io/reiyuchan" target="_blank" icon><v-icon>fab fa-keybase</v-icon></v-btn>
      </v-card-actions>
    </v-card>
    <v-card class="mx-auto my-5" max-width="700" title="Skills">
      <v-list lines="two">
        <v-list-item prepend-icon="mdi mdi-linux" title="Linux" subtitle="Linux Administration, User Settings" />
        <v-list-item prepend-icon="mdi mdi-server" title="IT" subtitle="Computer and Server Operations" />
        <v-list-item prepend-icon="mdi mdi-web" title="Web development" subtitle="JavaScript/TypeScript, Java, PHP, Go" />
        <v-list-item prepend-icon="mdi mdi-android" title="Mobile Development" subtitle="React Native, Cordova" />
        <v-list-item prepend-icon="mdi mdi-unity" title="Game development"
          subtitle="C#, Developing Game Systems, Sound Designer" />
      </v-list>
    </v-card>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({

})
</script>
