<template>
    <div>
        <v-container>
           <span class="display-1">How it works</span>
           <v-card
            elevation="7"
            class="mx-auto text-center"
           >
                <v-container>
                    <v-row justify="center">
                            <v-col cols="12" md="4" sm="12">
                                <v-avatar tile size="100">
                                    <v-icon>{{ testIcon }}</v-icon>
                                </v-avatar>
                                <p class="subtitle-1 font-weight-bold"  style="text-align: center !important;">Traders join Spak Trade</p>
                                <v-container>
                                    <v-card-text class="workText caption">
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab ratione, 
                                        eligendi nesciunt facere fuga adipisci 
                                        itaque odit error quasi unde similique enim impedit ex provident, hic molestias, quo dolorum modi!
                                    </v-card-text>
                                </v-container>
                            </v-col>

                            <v-col cols="12" md="4" sm="12">
                                <v-avatar tile size="100">
                                    <v-icon>{{ testIcon }}</v-icon>
                                </v-avatar>
                                <p class="subtitle-1 font-weight-bold" style="text-align: center !important;" id="workTitle">Traders join Spak Trade</p>
                                <v-container>
                                    <v-card-text class="workText caption">
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab ratione, 
                                        eligendi nesciunt facere fuga adipisci 
                                        itaque odit error quasi unde similique enim impedit ex provident, hic molestias, quo dolorum modi!
                                    </v-card-text>
                                </v-container>
                            </v-col>

                            <v-col cols="12" md="4" sm="12">
                                <v-avatar tile size="100">
                                    <v-icon>{{ testIcon }}</v-icon>
                                </v-avatar>
                                <p class="subtitle-1 font-weight-bold" style="text-align: center !important;" id="workTitle">Traders join Spak Trade</p>
                                <v-container>
                                    <v-card-text class="workText caption">
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab ratione, 
                                        eligendi nesciunt facere fuga adipisci 
                                        itaque odit error quasi unde similique enim impedit ex provident, hic molestias, quo dolorum modi!
                                    </v-card-text>
                                </v-container>
                            </v-col>
                    </v-row>
                </v-container>
           </v-card>
        </v-container>

        <!-- Sheet -->

        <v-sheet class="mt-8">
            <v-container>
                <v-row justify="center">
                    <v-col cols="12" md="4" sm="12">
                        <v-btn class="text-center purple darken-3 mr-2" large dark rounded block>Join as an investor</v-btn>
                    </v-col>
                    <v-col cols="12" md="4" sm="12">
                        <v-btn color="purple darken-3" large  rounded outlined block class="ml-2" >Join as an investor</v-btn>
                    </v-col>
                </v-row>
            </v-container>
        </v-sheet>

       <v-sheet class="tradeVolume mt-12">
           <div class="text-center">
               <v-card class="mx-auto volume" max-height="150" min-height="150" width="50%" elevation="12">
                   <v-contianer>
                       <v-row justify="start">
                           <v-card-text class="headline mt-12">Trading Volume</v-card-text>
                       </v-row>
                   </v-contianer>
               </v-card>

               <v-container>
                   <v-row>
                        <v-col cols="12" md="4" sm="12">
                            <span class="headline indigo--text text--darken-3">Performance</span>
                            <p class="text-center caption">Pick among the best Traders and instantly convert their advice into live trades.</p>

                            <v-card class="mt-5 mx-auto elevation-3">
                                <v-simple-table>
                                    <template v-slot:default>
                                        <thead>
                                            <tr>
                                                <th class="text-left">Trader</th>
                                                <th class="text-left">Amount</th>
                                                <th class="text-left">Investors</th>
                                            </tr>
                                        </thead>
                                        <tbody>
                                            <tr
                                                v-for="(item, i) in items"
                                                :key="i"
                                            >
                                                <td>{{ item.name }}</td>
                                                <td>{{ item.amount }}</td>
                                                <td>{{ item.investors }}</td>
                                            </tr>
                                        </tbody>
                                    </template>
                                </v-simple-table>
                            </v-card>
                        </v-col>

                        <v-col cols="12" md="4" sm="12">
                            <span class="headline indigo--text text--darken-3">Top Traders</span>
                            <p class="text-center caption">
                                Combined top 5 traders' performance $429,181 (66258.3 pips).
                            </p>

                            <v-card class="mt-10 mx-auto elevation-3" min-height="286">
                                <v-sparkline
                                    :fill="fill"
                                    :gradient="gradient"
                                    :line-width="width"
                                    height="200"
                                    :padding="padding"
                                    :smooth="radius || false"
                                    :value="value"
                                    auto-draw
                                ></v-sparkline>
                            </v-card>
                        </v-col>

                        <v-col cols="12" md="4" sm="12">
                            <span class="headline indigo--text text--darken-3">Market Sentiment</span>
                            <p class="text-center caption">Currency Pairs selected by ZuluTraders during the last 4 hours</p>

                            <v-card elevation="0" class="mt-5 mx-auto elevation-3" style="background-color: transparent !important;">
                                <v-row>
                                    <v-col cols="12" md="6">
                                        <v-card>
                                            <span>EUR/USD</span>
                                            <v-container>
                                                <v-progress-linear
                                                    :active="active"
                                                    :background-opacity="opacity"
                                                    :bottom="bottom"
                                                    :height="height"
                                                    :rounded="rounded"
                                                    :value="progressValue"
                                                    color="indigo"
                                                ></v-progress-linear>

                                                

                                                <v-spacer></v-spacer>
                                            </v-container>
                                            <v-divider class="mx-4"></v-divider>
                                            <v-card-actions>
                                                <v-btn text disabled class="buyBtn"><span class="buyBtn">buy</span><span class="buyBtnSub">15.4%</span></v-btn><br>


                                                <v-spacer></v-spacer>

                                                <v-btn text disabled class="sellBtn">sell<span class="sellBtnSub">15.4%</span></v-btn>
                                            </v-card-actions>
                                        </v-card>
                                    </v-col>

                                    <v-col cols="12" md="6">
                                        <v-card>
                                            <span>EUR/USD</span>
                                            <v-container>
                                                <v-progress-linear
                                                    :active="active"
                                                    :background-opacity="opacity"
                                                    :bottom="bottom"
                                                    :height="height"
                                                    :rounded="rounded"
                                                    :value="progressValue"
                                                    color="indigo"
                                                ></v-progress-linear>

                                                

                                                <v-spacer></v-spacer>
                                            </v-container>
                                            <v-divider class="mx-4"></v-divider>
                                            <v-card-actions>
                                                <v-btn text disabled class="buyBtn"><span class="buyBtn">buy</span><span class="buyBtnSub">15.4%</span></v-btn><br>


                                                <v-spacer></v-spacer>

                                                <v-btn text disabled class="sellBtn">sell<span class="sellBtnSub">15.4%</span></v-btn>
                                            </v-card-actions>
                                        </v-card>
                                    </v-col>

                                    <v-col cols="12" md="6">
                                        <v-card>
                                            <span>EUR/USD</span>
                                            <v-container>
                                                <v-progress-linear
                                                    :active="active"
                                                    :background-opacity="opacity"
                                                    :bottom="bottom"
                                                    :height="height"
                                                    :rounded="rounded"
                                                    :value="progressValue"
                                                    color="indigo"
                                                ></v-progress-linear>

                                                

                                                <v-spacer></v-spacer>
                                            </v-container>
                                            <v-divider class="mx-4"></v-divider>
                                            <v-card-actions>
                                                <v-btn text disabled class="buyBtn"><span class="buyBtn">buy</span><span class="buyBtnSub">15.4%</span></v-btn><br>


                                                <v-spacer></v-spacer>

                                                <v-btn text disabled class="sellBtn">sell<span class="sellBtnSub">15.4%</span></v-btn>
                                            </v-card-actions>
                                        </v-card>
                                    </v-col>

                                    <v-col cols="12" md="6">
                                        <v-card>
                                            <span>EUR/USD</span>
                                            <v-container>
                                                <v-progress-linear
                                                    :active="active"
                                                    :background-opacity="opacity"
                                                    :bottom="bottom"
                                                    :height="height"
                                                    :rounded="rounded"
                                                    :value="progressValue"
                                                    color="indigo"
                                                ></v-progress-linear>

                                                <v-spacer></v-spacer>
                                            </v-container>
                                            <v-divider class="mx-4"></v-divider>
                                            <v-card-actions>
                                                <v-btn text disabled class="buyBtn"><span class="buyBtn">buy</span><span class="buyBtnSub">15.4%</span></v-btn><br>

                                                <v-spacer></v-spacer>

                                                <v-btn text disabled class="sellBtn">sell<span class="sellBtnSub">15.4%</span></v-btn>
                                            </v-card-actions>
                                        </v-card>
                                    </v-col>
                                </v-row>
                            </v-card>
                        </v-col>
                    </v-row>
               </v-container>
           </div>

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

       <v-sheet>
           <v-row>
               <v-card flat>
                    <v-container>
                        <v-row justify="center">
                            <v-col cols="12" md="4" sm="12">
                                <v-card flat>
                                    <v-container>
                                        <v-row>
                                                <v-col cols="12" md="4" sm="6">
                                                    <v-img
                                                        src="@/assets/phone.svg"
                                                        contain
                                                    ></v-img>
                                                </v-col>
                                                <v-col cols="12" md="6" sm="6">
                                                    <h6 class="text-center font-weight-light pink--text text--darken-3" style="font-size: 1.1rem !important;"><span class="font-weight-bold">Spak</span> your mobile</h6>
                                                    <v-card-text style="text-align: left !important;">
                                                        Check out our Android, iPhone, iPad and desktop widget apps.
                                                    </v-card-text>
                                                    <v-card-actions class="text-center">
                                                        <v-btn dark color="pink darken-4" rounded style="text-transform: lowercase !important;">download now</v-btn>
                                                    </v-card-actions>
                                                </v-col>
                                            </v-row>
                                    </v-container>
                                </v-card>
                            </v-col>   

                            <v-divider vertical></v-divider>

                            <v-col cols="12" md="4" sm="12">
                                <v-card flat>
                                    <v-container>
                                        <v-card-title class="font-weight-light grey--text">testimonials: </v-card-title>
                                        <v-card-text class="body-1">
                                            <i>
                                                The social aspect with Traders makes for an educational experience and transparent service. 
                                                The analytics are very useful
                                            </i>
                                            </v-card-text>
                                            <p class="text-right"><b>Omar - AAA635899F</b></p>
                                    </v-container>
                                </v-card>
                            </v-col>
                            
                            <v-divider vertical></v-divider>

                            <v-col cols="12" md="3" sm="12">
                                <v-card flat>
                                    <v-container>
                                        <v-card-title class="font-weight-light grey--text">as seen in: </v-card-title>
                                        <v-card-text class="body-1 text-center">
                                            <v-avatar tile size="100">
                                                <v-icon>{{ newsIcon }}</v-icon>
                                            </v-avatar>
                                            </v-card-text>
                                    </v-container>
                                </v-card>
                            </v-col>
                        </v-row>
                    </v-container>
                </v-card>
           </v-row>
       </v-sheet>

        <v-sheet class="mt-5 account blue-grey lighten-5">
          <v-container>
              <h5 class="text-center title">Join us at Spaktrade</h5>
              <v-card-text style="text-align: center !important;" class="body-1">
                  Create a real money account
                    Or practise with a Demo
            </v-card-text>
            <v-container>
                <v-row>
                    <v-col cols="12" md="6" sm="12"></v-col>
                    <v-col cols="12" md="6" sm="12">
                        <v-card elevation="1">
                            <v-container>
                                <form action="">
                                    <v-row>
                                        <v-col cols="12" md="6" sm="6">
                                            <v-text-field
                                             label="First Name"
                                             outlined
                                             type="text"
                                             dense
                                             required
                                            ></v-text-field>
                                        </v-col>
                                        <v-col cols="12" md="6" sm="6">
                                            <v-text-field
                                             label="Last Name"
                                             outlined
                                             type="text"
                                             dense
                                             required
                                            ></v-text-field>
                                        </v-col>
                                         <v-col cols="12" md="12" sm="12">
                                            <v-text-field
                                             label="E-mail"
                                             type="email"
                                             outlined
                                             required
                                            ></v-text-field>
                                        </v-col>
                                        <v-col cols="12" md="12" sm="12">
                                            <v-text-field
                                             label="Password"
                                             type="password"
                                             outlined
                                             required
                                            ></v-text-field>
                                        </v-col>
                                    </v-row>
                                    <v-row>
                                        <v-col cols="12" md="3" sm="3">
                                            <v-select
                                                :items="items"
                                                :rules="[v => !!v || 'Item is required']"
                                                label="+234"
                                                required
                                                outlined
                                            ></v-select>
                                        </v-col>
                                        <v-col cols="12" md="9" sm="9">
                                            <v-text-field
                                             outlined
                                             label="phone number"
                                             type="number"
                                             required
                                            ></v-text-field>
                                        </v-col>
                                    </v-row>
                                    <v-row justify="center">
                                        <v-col cols="12" md="6" sm="6">
                                            <v-switch v-model="disabled" class="ma-2" label="Demo Account"></v-switch>
                                        </v-col>
                                        <v-col cols="12" md="6" sm="6">
                                            <v-switch v-model="disabled" class="ma-2" label="Real Account"></v-switch>
                                        </v-col>

                                        <v-container>
                                            <div class="text-center">
                                                <v-checkbox
                                                v-model="checkbox"
                                                :rules="[v => !!v || 'You must agree to continue!']"
                                                label="I have read and I accept the Terms and Conditions and the Privacy Policy of SpakTrade."
                                                required
                                            ></v-checkbox>
                                            </div>
                                        </v-container>
                                    </v-row>
                                    <div class="text-center">
                                        <v-container>
                                            <v-btn dark rounded block class="text-center indigo">Create Account</v-btn>
                                        </v-container>
                                    </div>
                                   <v-row justify="center">
                                       <v-col cols="12" md="3" sm="4"><v-divider></v-divider></v-col>
                                       <v-col cols="12" md="4" sm="4"><span class="ml-6 signUp">Or Sign up using </span></v-col>
                                       <v-col cols="12" md="3" sm="4"><v-divider></v-divider></v-col>
                                   </v-row>
                                    <v-row justify="center">
                                        <v-col cols="12" md="4" sm="6">
                                        <v-btn rounded block dark class="facebook font-weight-bold" style="text-transform: lowercase !important; font-size: 1.2rem !important;">facebook</v-btn>
                                        </v-col>
                                        <v-col cols="12" md="4" sm="6">
                                            <v-btn rounded outlined color="blue-grey darken-4" class="text--capitalize" block style="text-transform: none !important; font-size: 1.2rem !important;">
                                                <span class="googleB font-weight-bold">G</span>
                                                <span class="googleR font-weight-bold">o</span>
                                                <span class="googleY font-weight-bold">o</span>
                                                <span class="googleB font-weight-bold">g</span>
                                                <span class="googleG font-weight-bold">l</span>
                                                <span class="googleR font-weight-bold">e</span>
                                            </v-btn>
                                        </v-col>
                                    </v-row>
                                    <div class="text-center">
                                        <p class="caption blue-grey--text">We will never post anything without your permission</p>
                                    </div>
                                </form>
                            </v-container>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
          </v-container>
        </v-sheet>
    </div>
</template>


<script>
import { mdiSpeedometerMedium } from "@mdi/js";
import { mdiFindReplace } from "@mdi/js";
import { mdiSpeedometer } from "@mdi/js";
import { mdiHome } from '@mdi/js';
import { mdiNewspaper } from '@mdi/js';

//eslint-disable-next-line no-unused-vars
const gradients = [
    ['#222'],
    ['#42b3f4'],
    ['red', 'orange', 'yellow'],
    ['purple', 'violet'],
    ['#00c6ff', '#F0F', '#FF0'],
    ['#f72047', '#ffd200', '#1feaea'],
]

export default {
    data() {
        return {
            speedIcon1: mdiSpeedometerMedium,
            speedIcon2: mdiSpeedometer,
            findIcon: mdiFindReplace,
            testIcon: mdiHome,
            newsIcon: mdiNewspaper,
            
            // Sparkline
            fill: true,
            gradient: gradients[3],
            gradients,
            padding: 8,
            radius: 10,
            value: [0, 4, 6 ,7, 8 ,9 ,10, 6, 9 , 0],
            width: 2,

            // progress
            active: true,
            height: 7,
            progressValue: 30,


            items: [
                {
                    name: "Fujinch",
                    amount: "$4k",
                    investors: 19
                },
                {
                    name: "John smith",
                    amount: "$100",
                    investors: 2180
                },
                {
                    name: "Alex00",
                    amount: "$4k",
                    investors: 120
                },
                {
                    name: "PORTO",
                    amount: "$21",
                    investors: 69
                },
                {
                    name: "Veronica",
                    amount: "$67",
                    investors: 1109
                },
            ]
            
        }
    }
}
</script>

<style scoped>
    .title {
        font-size: 2.1rem !important;
    }

    .workText {
        transform: translateY(-2rem) !important;
    }
    .display-1 {
        font-size: 2.5rem !important;
    }
    .sheet2 {
        background-color: #edeef8 !important;
        border-radius: 0rem 0rem 0rem 11rem !important;
    }
    .subBuy {
        font-size: 0.8rem !important;
    }
    .xrow {
        padding: 0px !important;
        margin: 0px !important;
    }
    .card3 {
        border-radius: 20px !important;
        background-color: transparent !important;
    }
    .tradeVolume {
        background-color: #f8eafa;
        margin-top: 7rem !important;
    }
    .volume {
        transform: translateY(-4rem) !important;
    }
    .buyBtn {
        font-size: 0.7rem !important;
        color: #1A237E !important;
    }
    .sellBtn {
        font-size: 0.7rem !important;
    }
    .buyBtnSub {
        font-size: 0.5rem !important;
        color: #1A237E !important;
    }
    .sellBtnSub {
        font-size: 0.5rem !important;
    }
    .disc {
        background-color: transparent !important;
    }
    .signUp {
        transform: translateY(-1.5rem) !important;
    }
    .facebook {
        background-color:  #3b5998 !important;
    } 
    .googleB {
        color: #4885ed !important;
    }
    .googleG {
        color: #3cba54 !important;
    }
    .googleR {
        color: #db3236 !important;
    }
    .googleY {
        color: #f4c20d !important;
    }

</style>