<template>
    <div>
        <v-container>
            <v-row>
                <v-col
                cols="12"
                md="5"
                sm="12"
                >
                    <v-card flat>
                        <v-img
                        
                        ></v-img>
                    </v-card>
                </v-col>

                <v-col
                cols="12"
                md="7"
                sm="12"
                >
                
                    <v-card flat class="mx-auto">
                        <v-card-title class="font-weight-bold blue-grey--text text--darken display-1">100% stocks, 0% commission</v-card-title>


                        <v-card-text class="title font-weight-thin indigo--text text--darken-4 mt-2">
                            Why pay fees when you don’t have to? Invest in a large variety of stocks on eToro without 
                            paying any markups, ticketing or management fees. There are no limits on trading volume either.
                        </v-card-text>

                        <v-container>
                            <v-btn outlined large color="purple darken-4" class="ml-1 mt-1">Invest in stocks</v-btn>
                        </v-container>

                        <v-card-text class="blue-grey--text text--lighten-1 caption">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt a eveniet mollitia 
                            neque assumenda necessitatibus quasi numquam exercitationem, 
                            delectus aliquid sed vero beatae omnis voluptatibus esse hic maxime consequuntur. Tempore!
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt a eveniet mollitia 
                            neque assumenda necessitatibus quasi numquam exercitationem, 
                            delectus aliquid sed vero beatae omnis voluptatibus esse hic maxime consequuntur. Tempore!
                            <span><v-btn text class="ml-n2" color="blue-grey" style="font-size: 11px !important; text-transform: capitalize;">click here</v-btn></span>
                        </v-card-text>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>

        <!-- Sheet -->

        <v-sheet  class="sheet1">
            <v-container>
                <v-row class="mb-5 mt-5">
                    <v-container></v-container>
                    <v-col cols="12" md="6" sm="12">
                        <v-card class="mx-auto card1" elevation="5" v-for="n in 3" :key="n">
                            <v-row class="xrow">
                                <v-col cols="12" md="4" sm="12">
                                    <v-img
                                     src="@/assets/harvey.jpg"
                                     class="imgx"
                                     height="100%"
                                    ></v-img>
                                </v-col>
                                <v-col cols="12" md="6" sm="12">
                                    <v-card-title class="indigo--text font-weight-bold" style="font-size: 1.5rem !important;">harveyx2</v-card-title>
                                    <v-card-subtitle class="purple--text text--darkken-2 subtitle-2 font-weight-light" style="font-size: .9rem !important;">Harvey Spectar</v-card-subtitle>
                                    <v-card-text class="">
                                        <span class="lime--text font-weight-bold" style="font-size: 2rem !important;">10.8<span class="font-weight-light">%</span></span>
                                        <p class="overline grey--text text--lighten-1" style="font-size: .7rem !important;">gain (last 3m)</p>
                                    </v-card-text>
                                </v-col>
                                <v-divider vertical></v-divider>
                                <v-col cols="12" md="1" sm="12">
                                    <v-btn outlined class="ml-4" color="lime" style="transform: translateY(6rem) !important;">5</v-btn>
                                    <p class="overline blue-grey--text text--darken-3" style="text-align: center !important; font-size: 11px !important; transform: translateX(22.5px) !important;">risk</p>
                                </v-col>
                            </v-row>
                        </v-card>
                    </v-col>
                    <v-col cols="12" md="5" sm="12" class="ml-12">
                        <v-card flat class="mx-auto card3"> 
                            <v-card-text class="indigo--text display-1" style="font-size: 1.6rem !important;">
                                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius, voluptatem! Quasi, 
                                explicabo voluptatum. Esse fuga cumque expedita vitae. In quaerat 
                                blanditiis tempora optio odit magnam recusandae ex maiores itaque asperiores!
                            </v-card-text>

                            <v-btn large dark class="ml-4 mb-4 pink">Discover</v-btn>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-sheet>
        
        <v-sheet height="150"></v-sheet>
        <v-sheet class="sheet2 mt-12">
            <v-container>
                <v-row>
                    <v-col
                    cols="12"
                    md="6"
                    sm="12"
                    >
                        <v-card flat class="mx-auto disc">
                            <v-card-text class="mb-3 blue-grey--text body-1 mt-5">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam exercitationem maiores, sunt culpa consequatur in, 
                                qui voluptas ad amet est perspiciatis tenetur velit asperiores, 
                                alias atque nulla animi necessitatibus sequi?
                                Qooi voluptas ad amet est perspiciatis tenetur velit asperiores, 
                                alias atque nulla animi necessitatibus sequi?
                            </v-card-text>
                            <v-card-text style="text-align: center !important;" class="ml-n-5">
                                <v-icon size="100" color="pink darken-2">{{ speedIcon2 }}</v-icon>
                                <span class="purple--text font-weight-bold" style="font-size: 2rem !important;">221</span>
                            </v-card-text>
                        </v-card>

                        <v-btn large ripple outlined color="indigo">Explore<v-icon right>{{ speedIcon1 }}</v-icon></v-btn>
                        <v-btn large dark color="indigo" class="ml-2"><v-icon left>{{ findIcon }}</v-icon>discover people</v-btn>
                    </v-col>

                    <v-col
                    cols="12"
                    md="6"
                    sm="12"
                    >
                        <v-img
                        src="@/assets/discover.svg"
                        ></v-img>
                    </v-col>
                </v-row>
            </v-container>
        </v-sheet>

        <v-sheet height="100"></v-sheet>

        <v-sheet></v-sheet>
    </div>
</template>


<script>
import { mdiSpeedometerMedium } from "@mdi/js";
import { mdiFindReplace } from "@mdi/js";
import { mdiSpeedometer } from "@mdi/js";

export default {
    data() {
        return {
            speedIcon1: mdiSpeedometerMedium,
            speedIcon2: mdiSpeedometer,
            findIcon: mdiFindReplace,
            
        }
    }
}
</script>

<style scoped>
    .title {
        font-size: 2.1rem !important;
    }
    .display-1 {
        font-size: 2.5rem !important;
    }
    .sheet1 {
        background-color: white !important;
        border-radius: 0rem 11rem 0rem 11rem !important;
    }
    .disc {
        background-color: transparent !important;
    }
    .sheet2 {
        background-color: #edeef8 !important;
        border-radius: 0rem 0rem 0rem 11rem !important;
    }
    .xrow {
        padding: 0px !important;
        margin: 0px !important;
    }
    .card3 {
        border-radius: 20px !important;
        background-color: transparent !important;
    }
    .card1 {
        border-radius: 2.1rem 0rem 2.1rem 0rem !important;
        margin-bottom: 1rem !important;
    }
    .imgx {
        border-radius: 2.1rem 0rem 2.1rem 0rem !important;
    }

    .col-xl, .col-xl-auto, .col-xl-12, .col-xl-11, .col-xl-10, .col-xl-9, .col-xl-8, .col-xl-7, .col-xl-6, .col-xl-5, .col-xl-4, .col-xl-3, .col-xl-2, .col-xl-1, .col-lg, .col-lg-auto, .col-lg-12, .col-lg-11, .col-lg-10, .col-lg-9, .col-lg-8, .col-lg-7, .col-lg-6, .col-lg-5, .col-lg-4, .col-lg-3, .col-lg-2, .col-lg-1, .col-md, .col-md-auto, .col-md-12, .col-md-11, .col-md-10, .col-md-9, .col-md-8, .col-md-7, .col-md-6, .col-md-5, .col-md-4, .col-md-3, .col-md-2, .col-md-1, .col-sm, .col-sm-auto, .col-sm-12, .col-sm-11, .col-sm-10, .col-sm-9, .col-sm-8, .col-sm-7, .col-sm-6, .col-sm-5, .col-sm-4, .col-sm-3, .col-sm-2, .col-sm-1, .col, .col-auto, .col-12, .col-11, .col-10, .col-9, .col-8, .col-7, .col-6, .col-5, .col-4, .col-3, .col-2, .col-1 {
        width: 100%;
        padding: 0px;
    }
</style>