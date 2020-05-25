<template>
    <div class="profile pa-12 ma-3" app>
        <v-container fluid>
            <v-row justify="center" class="my-3">
                <v-avatar color="grey" size="100px">
                    <img src="https://i.vsco.co/5d590ef1a602775f0a2fdbe2?size=120&c=1&dpr=1">
                </v-avatar>
            </v-row>
            <v-row justify="center" class="my-3 font-weight-bold">
                <span>Name</span>
            </v-row>
            <v-row justify="center" class="my-3 grey--text">
                <span>username</span>
            </v-row>
            <v-row justify="center" class="my-3 grey--text">
                <span>description</span>
            </v-row>
            <v-row justify="center" class="my-3 grey--text">
                <span>social media</span>
            </v-row>
        </v-container>
        <v-container fluid>
            <v-layout 
                row
                wrap 
                pa-12
                justify-center
                
            >
                <v-flex xs5 sm4 md3 lg2
                ma-5
                    v-for="(data, index) in datas" 
                    :key="index"
                >
                    <v-img :src="data.urls.small"></v-img>
                </v-flex>
            </v-layout>
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
            photos: 30,
        }
    },
    methods:{
        searchPhoto(photos){
            return unsplash.search.photos("california", 1, photos)
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