<template>
  <v-app id="app" :theme="theme">
    <NavBar :theme="theme" :toggle-theme="toggleTheme" />
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import NavBar from '@/components/NavBar.vue'
import { defineComponent } from 'vue';

const THEME = "theme"

type DataType = {
  theme: string
}

export default defineComponent({
  name: 'App',
  components: {
    NavBar,
  },
  data(): DataType {
    return {
      theme: 'dark'
    }
  },
  methods: {
    toggleTheme() {
      if (this.theme === 'light') {
        this.theme = 'dark'
        localStorage.setItem(THEME, 'dark')
        return
      }
      this.theme = 'light'
      localStorage.setItem(THEME, 'light')
    }
  },
  created() {
    const storedTheme = localStorage.getItem(THEME)
    if (!storedTheme) {
      localStorage.setItem(THEME, this.theme)
      return
    }
    this.theme = storedTheme
  }
})
</script>

<style>
#app {
  background-image: url('@/assets/File_001.png');
  background-repeat: no-repeat;
  background-size: cover;
}
</style>