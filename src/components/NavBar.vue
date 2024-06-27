<template>
    <v-app-bar>
        <v-toolbar-title>reiyuchan.github.io</v-toolbar-title>
        <v-spacer />
        <div class="d-none d-sm-flex ga-4 pa-2">
            <v-btn to="/">Home</v-btn>
            <v-btn to="/repos">Repositories</v-btn>
        </div>
        <v-btn @click="toggleTheme"
            :class="{ 'border-dark': theme === 'light' ? true : false, 'border-light': theme === 'light' ? false : true }"
            icon>
            <v-icon>{{ theme === 'light' ? 'fas fa-sun' : 'fas fa-moon' }}</v-icon>
        </v-btn>
    </v-app-bar>
    <MobileNav />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import MobileNav from '@/components/MobileNav.vue'

export default defineComponent({
    props: ['theme', 'toggleTheme'],
    components: {
        MobileNav
    }
})
</script>

<style scoped>
.border-dark {
    &:hover {
        border-width: 2px;
        border-radius: 100%;
        border-color: black;
    }
}

.border-light {
    &:hover {
        border-width: 2px;
        border-radius: 100%;
        border-color: white;

    }
}
</style>