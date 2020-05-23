<template>
    <v-app-bar
        color="white"
        flat
        dark
        class="px-12 py-4"
    >
        <v-btn append icon tile light>
            <v-icon>mdi-magnify</v-icon>
        </v-btn>
        <v-btn icon tile light>
            <v-icon>mdi-account-outline</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text tile light><span class="text-uppercase">rexal</span></v-btn>
        <v-spacer></v-spacer>
        <v-btn text tile light><span class="text-capitalize">feed</span></v-btn>
        <v-btn text tile light><span class="text-lowercase">username</span></v-btn>
        <v-btn icon tile light>
            <v-icon>mdi-gamepad-circle-outline</v-icon>
        </v-btn>
        <v-btn icon tile light>
            <v-icon>mdi-cached</v-icon>
        </v-btn>
    </v-app-bar>
</template>

<script>
export default {

}
</script>

<style>

</style>