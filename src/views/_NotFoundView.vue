<template>
    <v-container class="fill-height d-flex flex-column justify-center align-center text-center ga-4">
        <v-card min-height="600" min-width="600"
            class="d-none d-sm-flex flex-column justify-center align-center text-center pa-8 max-h">
            <v-icon size="128">mdi mdi-alert-circle-outline</v-icon>
            <h1 class="text-h3 font-weight-bold">404</h1>
            <p class="text-subtitle-1">Oops! The page you are looking for does not exist.</p>
            <v-theme-provider :theme="$vuetify.theme.current.dark ? 'light' : 'dark'">
                <v-btn class="mt-4" to="/">Go Home</v-btn>
            </v-theme-provider>
        </v-card>
        <v-card class="d-flex d-sm-none flex-column justify-center align-center text-center pa-8 max-h">
            <v-icon size="128">mdi mdi-alert-circle-outline</v-icon>
            <h1 class="text-h3 font-weight-bold">404</h1>
            <p class="text-subtitle-1">Oops! The page you are looking for does not exist.</p>
            <v-theme-provider :theme="$vuetify.theme.current.dark ? 'light' : 'dark'">
                <v-btn class="mt-4" to="/">Go Home</v-btn>
            </v-theme-provider>
        </v-card>
    </v-container>
</template>
