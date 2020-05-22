<template>
    <div>
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
                    pa-4
                >
                    <v-img :src="data.urls.small"></v-img>
                    <div class="mt-1 font-weight-thin">{{ data.user.username }}</div>
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
            datas: {}
        }
    },
    beforeCreate(){
        unsplash.search.photos("california", 1, 50, { orientation: "portrait" })
        .then(toJson)
        .then(json => {
            this.datas = json.results
            console.log(this.datas)
        })
    }    
}
</script>

<style>

</style>