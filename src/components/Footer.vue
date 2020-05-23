<template>
    <div>
        <v-footer
            color="black"
            padless
            class="white--text"
        >
            <v-row
                no-gutters
                class="py-12"
                >
                <div
                    v-for="(footer, index) in footer"
                    :key="index"
                    color="white"
                    text
                    rounded
                    class="mx-12 caption font-weight-bold text-capitalize"
                >
                    {{ index }}
                    <div v-for="(item, index) in footer" :key="index"
                        class="font-weight-light caption"
                    >
                        <router-link to="/" class="white--text">{{ item }}</router-link>
                    </div>
                </div>
                <v-spacer></v-spacer>
                <div class="mr-12 caption font-weight-light">
                    © REXAL 2020. All rights reserved.
                </div>
            </v-row>
        </v-footer>
    </div>
</template>

<script>
export default {
    data() {
        return {
            footer:{
                company: ['about','careers'],
                community: ['guidelines','support','redeem'],
                legal: ['privacy','terms','disclosures'],
                contact: ['brands','press'],
            }
        }
    },
}
</script>

<style>
</style>