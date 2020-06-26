<template>
    <div>
        <app-bar />

        <v-main>
            <v-sheet>
                <v-card>
                    <v-tabs
                     v-model="tab"
                     icons-and-text
                    >
                        <v-tab-slider></v-tab-slider>

                        <v-tab href="#tab1" class="pink--text text--darken-3">
                            Top Traders
                            <v-icon>{{ topTIcon }}</v-icon>
                        </v-tab>

                        <v-tab href="#tab2" class="pink--text text--darken-3">
                            All Traders
                            <v-icon>{{ allTIcon }}</v-icon>
                        </v-tab>

                        <v-spacer></v-spacer>

                        <v-row>
                            <v-col cols="12" md="5" sm="5">
                                <v-text-field
                                rounded
                                label="Search for traders"    
                                solo     
                                color="grey"  
                                :prepend-inner-icon="searchIcon"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          
                                ></v-text-field>
                            </v-col>

                            <v-col cols="12" md="6" sm="5">
                               <v-btn outlined rounded color="pink darken-4" class="mt-2" style="float: right !important;">join as a trader</v-btn>
                            </v-col>
                        </v-row>
                    </v-tabs>
                    <v-divider></v-divider>
                    <v-tabs class="pink lighten-5">
                        <v-tab>All</v-tab>
                        <v-tab class="green--text">$ Live</v-tab>
                    </v-tabs>
                </v-card>

                <v-sheet>
                    <v-tabs-items v-model="tab">
                        <v-tab-item
                            id="tab1"
                        >
                            <v-card flat class="text-center">
                                <v-card-text>
                                    <v-btn outlined rounded color="pink darken-4">Load More...</v-btn>
                                </v-card-text>

                                <v-card-text class="body-1 blue-grey--text text--darken-4 mt-5">
                                    No data
                                </v-card-text>

                                <v-container style="bottom: 0px !important;" class="mt-12">
                                    <p class="text-center">We do not recommend or make any implications about the future performance of any of these systems.</p>
                                </v-container>
                            </v-card>
                        </v-tab-item>
                    </v-tabs-items>
                </v-sheet>
            </v-sheet>
        </v-main>
        <footer-app />
    </div>
</template>


<script>
import AppBar from '@/components/core/AppBar.vue';
import Footer from '@/components/core/Footer.vue';
import { mdiAccountMultipleOutline } from "@mdi/js";
import { mdiAccountMultiplePlusOutline } from "@mdi/js";
import { mdiMagnify } from "@mdi/js";


export default {
    components: {
        'app-bar': AppBar,
        'footer-app': Footer,
    },

    data() {
        return {
            // Icons
            topTIcon: mdiAccountMultipleOutline,
            allTIcon: mdiAccountMultiplePlusOutline,
            searchIcon: mdiMagnify,

            // Js code
            tab: null,
        }
    }
}
</script>

<style scoped>
    .theme--light.v-tabs > .v-tabs-bar .v-tab:not(.v-tab--active), .theme--light.v-tabs > .v-tabs-bar .v-tab:not(.v-tab--active) > .v-icon, .theme--light.v-tabs > .v-tabs-bar .v-tab:not(.v-tab--active) > .v-btn, .theme--light.v-tabs > .v-tabs-bar .v-tab--disabled {
        color: rgba(167, 15, 121, 0.103);
    }
</style>
