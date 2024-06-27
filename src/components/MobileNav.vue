<template>
    <v-bottom-navigation class="d-flex d-sm-none">
        <v-btn to="/" class="text-uppercase"><v-icon>fas fa-home</v-icon>Home</v-btn>
        <v-btn to="/repos" class="text-uppercase"><v-icon>fab fa-github</v-icon>Repositories</v-btn>
    </v-bottom-navigation>
</template>

<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({
})
</script>

<style scoped></style>