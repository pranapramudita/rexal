<template>
    <div class="home caption">
        <v-container fluid>
            <v-layout 
                row 
                wrap 
                pa-12 
                justify-center
            >
                <v-flex 
                    xs5 sm4 md3 lg2 
                    v-for="(data, index) in datas" 
                    :key="index"
                    align-self-end
                    ma-5
                >
                    <v-img :src="data.urls.small"></v-img>
                    <div class="mt-1 font-weight-thin">{{ data.user.username }}</div>
                </v-flex>
            </v-layout>
            <v-container fluid>
                <v-layout row wrap justify-center>
                    <v-btn 
                        depressed 
                        tile 
                        class="white--text caption align-center mb-6" 
                        color="black" 
                        @click="morePhoto()"
                    >
                        load more
                    </v-btn>
                    </v-layout>
            </v-container>
        </v-container>
    </div>
</template>

<script>
import unsplash from '../plugins/unsplash'
import { toJson } from "unsplash-js";

export default {
    data() {
        return {
            datas: {},
            photos: 10,
        }
    },
    methods:{
        searchPhoto(photos){
            return unsplash.search.photos("vsco", 1, photos)
            .then(toJson)
            .then(json => {
                this.datas = json.results
                console.log(this.datas)
            })
        },
        morePhoto(){
            this.photos += 10
            this.searchPhoto(this.photos)
        },
    },
    created(){
        this.searchPhoto(this.photos)
    }    
}
</script>

<style>
</style>