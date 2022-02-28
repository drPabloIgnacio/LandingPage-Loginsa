<template>
    <div>
        <v-navigation-drawer
        v.model="drawer"
        app
        temporary
        dark
        >
        <v-list>
            <v-list-item>
                <v-list-item-avatar>
                    <!-- <img src="@/assets/img/logo.png" alt="logo"> -->
                </v-list-item-avatar>
                <v-list-item-conent>
                    <v-list-item-tittle class="title">Loginsa</v-list-item-tittle>
                    <v-list-item-subtitle>WEB</v-list-item-subtitle>
                </v-list-item-conent>
            </v-list-item>
        </v-list>

        <v-divider />

        <v-list dense>
            <v-list-item
            v-for="([icon, text, link], i) in items"
            :key="i"
            link
            @click="$vuetify.goTo(link)"
            >
                <v-list-item-icon class="justify-center">
                    <v-icon>{{ icon }}</v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                    <v-list-item-tittle class="subtitile-1">
                    {{ text }}
                    </v-list-item-tittle>
                </v-list-item-content>
            </v-list-item>
        </v-list>
        </v-navigation-drawer>

        <v-app-bar
        app
        :color="color"
        :flat="flat"
        dark
        class="px-15"
        :class="{ expand: flat}"
        >
            <v-toolbr-title>
                <!-- <v-img src="@/assets/img/logo.png" max-width="50px" /> -->
            </v-toolbr-title>
            <v-spacer />
            <v-app-bar-nav-icon
                @click.stop="drawer = !drawer"
                class="mr-4"
                v-if="isXs"
            />
            <div v-else>
                <v-btn text @click="$vuetify.goTo('#hero')">
                    <span class="mr-2">Home</span>
                </v-btn>
            </div>

        </v-app-bar>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>