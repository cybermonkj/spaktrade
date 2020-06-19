<template>
    <div>
        <v-app-bar
         app
         dark
         shrink-on-scroll
         prominent
         id="appbar"
         class="bar"
        >
            <v-app-bar-nav-icon></v-app-bar-nav-icon>

            <v-toolbar-title>Spak Trade</v-toolbar-title>

            <v-spacer></v-spacer>

            <v-btn icon><v-icon>{{ searchIcon }}</v-icon></v-btn>
            <div class="hidden-md-and-down">
                <v-btn 
                 v-for="(bar, i) in barItems"
                 :key="i"
                 text
                 router :to="bar.to"
                 class="ml-1 mr-1"
                >{{ bar.title }}<v-icon right>{{ bar.icon }}</v-icon></v-btn>
            </div>
        </v-app-bar>
    </div>
</template>


<script>
import { mdiTrademark } from '@mdi/js';
import { mdiShopping } from '@mdi/js';
import { mdiTrendingUp } from '@mdi/js';
import { mdiCastEducation } from '@mdi/js';
import { mdiSkypeBusiness } from '@mdi/js';
import { mdiMagnify } from '@mdi/js';


export default {
    data() {
        return {
            searchIcon: mdiMagnify, 
            barItems: [
                { title: "Trading", icon: mdiTrademark, to: "/" },
                { title: "Top Markets", icon: mdiShopping, to: "#!" },
                { title: "Ivesting", icon: mdiTrendingUp, to: "#!" },
                { title: "Education", icon: mdiCastEducation, to: "#!" },
                { title: "Company", icon: mdiSkypeBusiness, to: "#!" }
            ]
        }
    }
}
</script>


<style scoped>
    
        /* //background: linear-gradient(to buttom right, #1A237E, #1A237E) !important; */
    .bar {
        /* background-image: linear-gradient(to bottom right, #F44336, #E65100, #FFEB3B); */
        background-image: linear-gradient(to bottom left, #1A237E, #4A148C, #880E4F);
    }
</style>