<template>
    <v-app id="inspire">
        <v-container>
            <h1>Checkout</h1>

            <v-stepper v-model="e6" style="background: none; box-shadow: none;" >
                <v-stepper-header style="background: none; box-shadow: none;">
                    <v-stepper-step
                            complete
                            editable
                            :complete="e6 > 1"
                            step="1"
                    >
                        Select campaign settings
                    </v-stepper-step>

                    <v-divider></v-divider>

                    <v-stepper-step
                            complete
                            :complete="e6 > 2" step="2"
                    >Create an ad group</v-stepper-step>

                    <v-divider></v-divider>

                    <v-stepper-step
                            step="3"
                            editable
                    >
                        Create an ad
                    </v-stepper-step>
                </v-stepper-header>

                <v-stepper-content step="1">
                    <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
                    <v-btn color="primary" @click="e6 = 2">Continue</v-btn>
                    <v-btn text>Cancel</v-btn>
                </v-stepper-content>

                <v-stepper-content step="2">
                    <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
                    <v-btn color="primary" @click="e6 = 3">Continue</v-btn>
                    <v-btn text>Cancel</v-btn>
                </v-stepper-content>
            </v-stepper>



        </v-container>

    </v-app>
</template>

<script lang="ts">
    import {Component, Vue} from "vue-property-decorator";

    @Component
    export default class Checkout extends Vue {
        e6: number = 1;
    }
</script>

<style>
    .container-main { background-color: #f4f4f4 }



    .container-principal {
        position: relative;
        top: 66px;
        padding: 0px 0px 0px 0px !important;
    }





</style>
