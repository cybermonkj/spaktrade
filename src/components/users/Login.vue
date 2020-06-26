<template>
   <div>
       <app-bar />

        <v-main class="text-center">
            <v-container>
                <h5 class="display-1 font-weight-medium text-cenmter grey--text text--darekn-1">Join us at SpakTrade</h5>
                <v-container>
                    <p class="text-center body-1 font-weight-medium">Create a real money account
                        Or practise with a Demo
                    </p>
                </v-container>
                <v-row justify="center">
                    <v-col cols="12" md="6" sm="12">
                        <v-card flat elevation="0" style="background-color: transparent !important;">
                            <v-container>
                                <v-row justify="center">
                                    <v-col cols="12" md="4" sm="4">
                                        <v-avatar tile size="50">
                                            <v-img
                                                src="@/assets/password.svg"
                                            ></v-img>
                                        </v-avatar>
                                    </v-col>

                                    <v-col cols="12" md="8" sm="8">
                                        <v-card-text>
                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore veniam 
                                        </v-card-text>
                                    </v-col>
                                     <v-col cols="12" md="4" sm="4">
                                        <v-avatar tile size="50">
                                            <v-img
                                                src="@/assets/password.svg"
                                            ></v-img>
                                        </v-avatar>
                                    </v-col>

                                    <v-col cols="12" md="8" sm="8">
                                        <v-card-text>
                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore veniam 
                                        </v-card-text>
                                    </v-col>

                                     <v-col cols="12" md="4" sm="4">
                                        <v-avatar tile size="50">
                                            <v-img
                                                src="@/assets/password.svg"
                                            ></v-img>
                                        </v-avatar>
                                    </v-col>

                                    <v-col cols="12" md="8" sm="8">
                                        <v-card-text>
                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore veniam 
                                        </v-card-text>
                                    </v-col>

                                     <v-col cols="12" md="4" sm="4">
                                        <v-avatar tile size="50">
                                            <v-img
                                                src="@/assets/password.svg"
                                            ></v-img>
                                        </v-avatar>
                                    </v-col>

                                    <v-col cols="12" md="8" sm="8">
                                        <v-card-text>
                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore veniam 
                                        </v-card-text>
                                    </v-col>
                                </v-row>
                            </v-container>
                        </v-card>
                    </v-col>

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
                                                required
                                            ></v-text-field>
                                        </v-col>
                                        <v-col cols="12" md="6" sm="6">
                                            <v-text-field
                                                label="Last Name"
                                                outlined
                                                type="text"
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
        </v-main>

       <footer-app />
   </div>
</template>


<script>
import AppBar from '@/components/core/AppBar.vue';
import Footer from '@/components/core/Footer.vue';


export default {
    components: {
        'app-bar': AppBar,
        'footer-app': Footer,
    },

    data() {
        return {
            
        }
    }
}
</script>


<style scoped>
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