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
            <v-btn router to="/login" color="white" rounded outlined>Login</v-btn>

        </v-app-bar>
    </div>
</template>


<script>
import { mdiTrademark } from '@mdi/js';
import { mdiShopping } from '@mdi/js';
import { mdiFeatureSearchOutline } from '@mdi/js';
import { mdiBitcoin } from '@mdi/js';
import { mdiContactsOutline } from '@mdi/js';
import { mdiMagnify } from '@mdi/js';
// import Login from '@/components/users/Login.vue';
// import SignUp from '@/components/users/Signup.vue';


export default {
    components: {
        // 'login': Login,
        // 'sign-up': SignUp,
    },

    data() {
        return {
            searchIcon: mdiMagnify, 
            barItems: [
                { title: "Traders", icon: mdiTrademark, to: "/" },
                { title: "Combos", icon: mdiShopping, to: "#!" },
                { title: "Cryptos", icon: mdiBitcoin, to: "#!" },
                { title: "Features", icon: mdiFeatureSearchOutline, to: "#!" },
                { title: "Contact Us", icon: mdiContactsOutline, to: "#!" }
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