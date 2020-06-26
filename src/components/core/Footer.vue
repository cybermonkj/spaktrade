<template>
  <v-footer
    dark
    padless                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             
  >
    <v-card
      flat
      tile
      class="indigo darken-4 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>

      <v-container>
        <v-row justify="center">
            <v-col cols="12" md="6" sm="12">
                <v-list disabled class="indigo darken-3 listz">
                    <v-card-title class="text-center font-weight-bold" style="text-align: center !important;">Connect</v-card-title>
                    <v-card-text style="text-align: left !important;">
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                        Aspernatur tempore quo eum. Deserunt perferendis incidunt 
                        corporis est, alias repudiandae 
                        ullam sunt soluta qui, ipsa provident quia animi voluptates eos beatae!
                    </v-card-text>
                </v-list>
            </v-col>

            <v-col cols="12" md="5" sm="12">
                <v-sheet color="indigo darken-4">
                    <v-form>
                        <v-text-field
                        label="Contact Us"
                        outlined
                        rounded
                        solo
                        color=""
                        ></v-text-field>
                    </v-form>
                </v-sheet>

                <v-btn >send <v-icon right>{{ sendIcon }}</v-icon></v-btn>
            </v-col>
        </v-row>
    </v-container>

      <v-divider></v-divider>

      <v-card-text class="white--text grey darken-4">
        {{ new Date().getFullYear() }} — <strong class="overline">spak trade</strong><span class="ml-2" id="footer-text">© Copyright All Rights reserved</span>
      </v-card-text>
    </v-card>
  </v-footer>
</template>


<script>
import { mdiSendCircleOutline } from "@mdi/js";

  export default {
    data: () => ({
        sendIcon: mdiSendCircleOutline,
        icons: [
        'fab fa-facebook',
        'fab fa-twitter',
        'fab fa-google-plus',
        'fab fa-linkedin',
        'fab fa-instagram',
        ],
        footerItems: [
            { text: "Lorem Ipsum Dolor", icon: mdiSendCircleOutline },
            { text: "Lorem Ipsum Dolor", icon: mdiSendCircleOutline },
            { text: "Lorem Ipsum Dolor", icon: mdiSendCircleOutline },
            { text: "Lorem Ipsum Dolor", icon: mdiSendCircleOutline },
            { text: "Lorem Ipsum Dolor", icon: mdiSendCircleOutline },
        ]
    }),
  }
</script>

<style scoped>
    #footer-text {
        text-transform: capitalize !important;
    }
    .listz {
        border-radius: 2rem 0rem 2rem 0rem !important;
    }
</style>