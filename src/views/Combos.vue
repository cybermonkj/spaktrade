<template>
    <div>
        <app-bar />

        <v-main>
            <v-sheet>
                <v-card flat class="text-center">
                    <v-container>
                        <span class="display-2 font-weight-bold grey--text text--darken-1">Traders Combos</span>
                    </v-container>
                    <p class="body-1 blue-grey--text text--darken-3">Choose among diversified Strategies built from combinations of our best Traders.</p>

                    <v-img
                     src="@/assets/hero-banner.gif"
                     width="100%"
                    ></v-img>
                </v-card>
                                                                                                                                                                                                                                              
            </v-sheet>
            <v-sheet>
                <v-card flat class="text-center">
                    <v-container>
                        <v-card-text class="display-1 grey--text text--darken-4" style="">What are Traders' Combos?</v-card-text>
                    </v-container>

                    <v-row justify="center" class="mt-3">
                        <v-col cols="12" md="4" sm="12">
                            <v-avatar tile size="80">
                                <v-img
                                  src="@/assets/web-hosting.svg"
                                  contain
                                ></v-img>
                            </v-avatar>
                            <h6 class="body-1 mt-2 grey--text text--darken-1 font-weight-bold">Managing Trading Services</h6>
                            <v-container>
                                <v-card-text class="mt-n4">
                                    <p class="body-3 font-weight-light">by SpakTrade’s Certified Management Portfolio Team.</p>
                                </v-card-text>
                            </v-container>
                        </v-col>

                        <v-col cols="12" md="4" sm="12">
                            <v-avatar tile size="80">
                                <v-img
                                  src="@/assets/speed-test.svg"
                                  contain
                                ></v-img>
                            </v-avatar>
                            <h6 class="body-1 mt-2 grey--text text--darken-1 font-weight-bold">High Performance Traders</h6>
                            <v-container>
                                <v-card-text class="mt-n4">
                                    <p class="body-3 font-weight-light">are grouped in dynamic combinations which correspond to a variety of risk appetites and strategies to follow.</p>
                                </v-card-text>
                            </v-container>
                        </v-col>

                        <v-col cols="12" md="4" sm="12">
                            <v-avatar tile size="80">
                                <v-img
                                  src="@/assets/analytics.svg"
                                  contain
                                ></v-img>
                            </v-avatar>
                            <h6 class="body-1 mt-2 grey--text text--darken-1 font-weight-bold">Full auto-pilot or Semi-automation?</h6>
                            <v-container>
                                <v-card-text class="mt-n4">
                                    <p class="body-3 font-weight-light">The simple and advanced version of Combos cover all trading profiles. 
                                        From passive/novice to experts/hands-on Investors.</p>
                                </v-card-text>
                            </v-container>
                        </v-col>
                    </v-row>

                    <v-row justify="center" class="mt-5 mb-3">
                        <v-btn rounded dark color="indigo darken-3">Select your combos!</v-btn>
                    </v-row>
                </v-card>
            </v-sheet>

            <v-sheet class="indigo darken-4 mt-5">
                <v-container>
                    <v-card flat class="text-center mx-auto" style="background-color: transparent !important;">
                        <h6 class="display-2 white--text" >What is your Combo Choice?</h6>
                    </v-card>

                    <v-card flat class="mb-12 mt-4">
                        <v-container>
                            <v-simple-table>
                                <template v-slot: default>
                                    <thead>
                                        <tr>
                                            <th class="text-left"></th>
                                            <th class="text-left">Combos</th>
                                            <th class="text-left"> Combos plus </th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr
                                         v-for="(item, i) in items"
                                         :key="i"
                                        >
                                            <td color="purple--text text--darken-2">{{ item.detail }}</td>
                                            <td><v-icon color="purple">{{ item.combos }}</v-icon></td>
                                            <td><v-icon color="purple">{{ item.combosplus }}</v-icon></td>
                                        </tr>
                                    </tbody>
                                </template>
                            </v-simple-table>
                        </v-container>
                    </v-card>
                </v-container>
            </v-sheet>

            <v-sheet>
                <v-container>
                    <v-row justify="center">
                        <v-card flat class="text-center">
                            <h6 class="display-1 font-weight-medium">How does Spaktrade select Traders for the Combos?</h6>
                            <v-container>
                                <p class="body-1 text-center">The Traders that are included in Combos have among other qualities</p>
                            </v-container>

                            <v-row justify="center">
                                <v-col cols="12" md="6" sm="12">
                                    <v-avatar tile size="60">
                                        <v-icon color="purple">{{ percentIcon }}</v-icon>
                                    </v-avatar>
                                    <v-card-text class="body-1 font-weight-medium mt-2">
                                        A Win % above 30%
                                    </v-card-text>
                                </v-col>
                                <v-col cols="12" md="6" sm="12">
                                    <v-avatar tile size="60">
                                        <v-icon color="purple">{{ chartIcon }}</v-icon>
                                    </v-avatar>
                                    <v-card-text class="body-1 font-weight-medium mt-2">
                                        A long-term positive ROI
                                    </v-card-text>
                                </v-col>
                                <v-col cols="12" md="6" sm="12">
                                    <v-avatar tile size="60">
                                        <v-icon color="purple">{{ numberIcon }}</v-icon>
                                    </v-avatar>
                                    <v-card-text class="body-1 font-weight-medium mt-2">
                                        Have executed more than 100 trades
                                    </v-card-text>
                                </v-col>
                                <v-col cols="12" md="6" sm="12">
                                    <v-avatar tile size="60">
                                        <v-icon color="purple">{{ chartIcon2 }}</v-icon>
                                    </v-avatar>
                                    <v-card-text class="body-1 font-weight-medium mt-2">
                                        A stable trading activity of at least 15 weeks
                                    </v-card-text>
                                </v-col>
                            </v-row>

                            <v-btn rounded color="indigo darken-3" dark class="mt-5 mb-3">Select your Combos</v-btn>
                        </v-card>
                    </v-row>
                </v-container>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    
            </v-sheet>
        </v-main>

        <footer-app />
    </div>
</template>


<script>
import AppBar from '@/components/core/AppBar.vue';
import Footer from '@/components/core/Footer.vue';
import { mdiPercentOutline } from "@mdi/js";
import { mdiChartBellCurve } from "@mdi/js";
import { mdiNumeric10CircleOutline } from "@mdi/js";
import { mdiChartTimeline } from "@mdi/js";
import { mdiMarkerCheck } from "@mdi/js";
import { mdiConsoleLine } from "@mdi/js";


export default {
    components: {
        'app-bar': AppBar,
        'footer-app': Footer,

    },

    data() {
        return {
            // Icon
            percentIcon: mdiPercentOutline,
            chartIcon: mdiChartBellCurve,
            numberIcon: mdiNumeric10CircleOutline,
            chartIcon2: mdiChartTimeline,

            items: [
                {
                    detail: "Portfolio Initialization (receive trades automatically)",
                    combos: mdiMarkerCheck,
                    combosplus: mdiMarkerCheck,
                },
                {
                    detail: "Portfolio Initialization (receive trades automatically)",
                    combos: mdiConsoleLine,
                    combosplus: mdiMarkerCheck,
                },
                {
                    detail: "Portfolio Initialization (receive trades automatically)",
                    combos: mdiConsoleLine,
                    combosplus: mdiMarkerCheck,
                },
            ]
        }
    }
}
</script>
